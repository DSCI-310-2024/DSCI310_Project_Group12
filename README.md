# Predictive Modelling: German Credit Risk 
 
## Table Of Contents  
- [Project Title](#project-title)
- [Authors](#authors)
- [About](#about)
- [Data Description](#data-description)
- [Report](#report)
- [Usage](#usage)
- [Docker](#docker)
- [Dependencies](#dependencies)
- [License](#license)
- [References](#references)

## Authors
- Shahrukh Islam Prithibi
- Sophie Yang
- Yovindu Don
- Jade Bouchard

## About
The goal of our analysis is to classify whether someone is a good or bad credit risk using attributes such as Credit History, Duration, and Residence. Our best-performing model is a Random Forest model. This model gave us an accuracy of 0.8 on unseen data, a decent result compared to the dummy model's accuracy of 0.7. We also obtained a precision score of 0.8, a recall score of 0.95, and F1 Score of 0.87. Our model performs decently well in terms of identifying people who are a good credit risk. However, if this model is to have a hand in real-world decision-making, precision should be improved to minimize classifying poor credit risks as good credit risks (false positives). In addition, more research should be done to ensure the model produces fair and equitable recommendations.

## Data Description
The Statlog (German Credit Data) dataset, sourced from [this UCI’s Machine Learning Repository](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data), used for classifying individuals as good or bad credit risks based on a variety of attributes. A cost matrix is required for evaluation, where misclassification costs are outlined. The cost matrix indicates that it is worse to classify a customer as good when they are bad, compared to classifying a customer as bad when they are good. The dataset contains 1000 instances with 20 features. Each feature has a different role, type, and demographic information.

## Report
The final report can be found
[here](https://github.com/DSCI-310-2024/DSCI310_Project_Group_12/blob/main/reports/credit_risk_analysis.ipynb)

## Usage

First time running the project,
run the following from the root of this repository:

``` bash
conda env create --file environment.yml
```

To run the analysis,
run the following from the root of this repository:

``` bash
jupyter lab 
```

Open `reports/credit_risk_analysis.ipynb` in Jupyter Lab
and under Switch/Select Kernel choose 
"Python [conda env:credit_risk_predictor]".

Next, under the "Kernel" menu click "Restart Kernel and Run All Cells...".

## Docker

Build and run the project using Docker with the following commands:

First, ensure you have Docker installed and running on the machine. Clone this repository and navigate to the directory.
Build the Docker image:
```bash
docker build -t yovindu/project .
```

Run the Docker container:
```bash
docker run -it --rm -p 8888:8888 -v "${PWD}":/home/jovyan yovindu/project
```
(Below instructions copied form this [repository](https://github.com/ttimbers/breast_cancer_predictor_py?tab=readme-ov-file#working-with-the-project-in-the-container-using-jupyter-lab))
In the terminal, look for a URL that starts with http://127.0.0.1:8888/lab?token= . Copy and paste that URL into your browser.

You should now see the Jupyter lab IDE in your browser, with all the project files visible in the file browser pane on the left side of the screen.

Open a terminal at the project root in the IDE. Use command `make clean-all` to reset the project to a clean state (i.e., remove all files generated by previous runs of the analysis). To run the analysis in its entirety, enter the command `make all` in the terminal in the project root.

## Dependencies

- `conda` (version 23.9.0 or higher)
- `nb_conda_kernels` (version 2.3.1 or higher)
- Python and packages listed in [`environment.yml`](environment.yml)

## License

The Credit Risk Analysis report contained herein is licensed under the
[Creative Commons Attribution 4.0 International (CC BY 4.0) License](https://creativecommons.org/licenses/by/4.0/legalcode).
See [the license file](LICENSE.md) for more information. If
re-using/re-mixing please provide attribution and link to this webpage.
The software code contained within this repository is licensed under the
MIT license. See [the license file](LICENSE.md) for more information.

## References

Costa e Silva, E., Lopes, I. C., Correia, A., & Faria, S. (2020). A logistic regression model for consumer default risk. Journal of Applied Statistics, 47(13-15), 2879–2894. <https://doi.org/10.1080/02664763.2020.1759030>

Dobby, C., & Vossos, T. (2024, February 22). Wall Street to Follow Canada’s Hot Risk Transfer Trade. Bloomberg.com. <https://www.bloomberg.com/news/articles/2024-02-22/wall-street-to-follow-canada-s-hot-capital-relief-trade>

Goraieb, E., Kumar, S., & Pepanides, T. (n.d.). Credit Risk | Risk & Resilience | McKinsey & Company. <https://www.mckinsey.com/capabilities/risk-and-resilience/how-we-help-clients/credit-risk>

Personal characteristics, grounds of discrimination protected in the BC Human Rights Code - BC Human Rights Tribunal. (2023, May 9). BC Human Rights Tribunal. <https://www.bchrt.bc.ca/human-rights-duties/personal-characteritics/>

# Medicalstatistic Interactive Teaching Labs  

This repository contains a collection of interactive teaching labs used in Medical Statistics lectures. Each lab is a self contained HTML page that runs entirely in the browser. The portal page `index.html` lists all available labs with search functionality.  

## Local development  

1. Clone the repository and install the Jekyll dependencies:  

```bash  
bundle install  
```  

2. Run the site locally using Jekyll to preview changes:  

```bash  
bundle exec jekyll serve --livereload  
```  

The site will be available at `http://localhost:4000`. Use the `--livereload` option so that changes refresh automatically.  

3. Edit or add HTML files in the root of the repository to create or update labs. Jekyll is configured via `_config.yml` to include all `.html` files in the site.  

## Deployment  

GitHub Pages is configured to build and publish the site from the `main` branch. Simply commit and push your changes to `main` and GitHub will rebuild and deploy the site automatically. The live site is available at:  

https://samsurtee.github.io/Medicalstatistic/  

The build pipeline uses the [`github-pages`](https://rubygems.org/gems/github-pages) gem and a simple `_config.yml` with the `modernist` remote theme.  

## Content map  

| Lab | Description/Notes |  
|---|---|  
| `index.html` | Portal page with navigation and search for the interactive labs. |  
| `OLS Linear Regression_Interactive Teaching Lab.html` | Interactive demonstration of ordinary least squares linear regression. |  
| `Parameter Estimator_Medical Statistics.html` | Tool for exploring parameter estimators in medical statistics. |  
| `chi_square_lab.html` | Chi square distribution and hypothesis testing lab. |  
| `mle_logistic_interactive.html` | Logistic regression maximum likelihood estimation interactive. |  
| `normal_distribution.html` | Visualisation of the normal distribution and its properties. |  
| `qualitative_stats_interactive.html` | Interactive module covering qualitative statistical analysis. |  
| `quantitative_descriptive_statistics_single_file_teaching_page.html` | Interactive demo of descriptive statistics for quantitative data. |  
| `t_distribution_demo_fixed.html` | Demonstration of the Student’s t distribution. |  
| `动态置信区间演示.html` | Dynamic confidence interval demonstration (in Chinese). |  
| `qrcode.png` | QR code image used on the portal page. |  

To add a new interactive lab, place a new `.html` file in the root directory and link to it from `index.html` so it appears in the portal.

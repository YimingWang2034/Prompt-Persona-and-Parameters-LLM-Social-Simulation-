# PolyPersona: Virtual Persona Generation for Energy Trading Research

## Project Overview

This repository contains a comprehensive framework for generating virtual personas to study energy trading preferences and decision-making patterns in peer-to-peer energy markets. The project focuses on analyzing how different demographic characteristics, political ideologies, and environmental attitudes influence energy trading decisions across various social groups and organizations.

## Project Structure

### Core Persona Generation Scripts

The main persona generation scripts create virtual individuals with specific demographic profiles and analyze their energy trading preferences:

- **`polypersona.py`** - Main German persona generation script that creates 1000 virtual German citizens with comprehensive demographic profiles
- **`polypersonaAgeYoung.py`** - Generates personas with young age characteristics for age-related sensitivity analysis
- **`polypersonaCC1.py`** - Creates personas with climate change attitude level 1 for climate sensitivity analysis
- **`polypersonaCC7.py`** - Generates personas with climate change attitude level 7 for climate sensitivity analysis
- **`polypersonaEducationHigh.py`** - Creates personas with high education levels for education sensitivity analysis
- **`polypersonaEmploymentNone.py`** - Generates unemployed personas for employment status sensitivity analysis
- **`polypersonaLuckyNumber.py`** - Creates personas with specific lucky number preferences for behavioral analysis
- **`polypersonaNoAge.py`** - Generates personas without age specifications for age-neutral analysis
- **`polypersonaNoCC.py`** - Creates personas without climate change attitudes for neutral climate analysis
- **`polypersonaNoEdu.py`** - Generates personas without education specifications for education-neutral analysis
- **`polypersonaNoEmploy.py`** - Creates personas without employment specifications for employment-neutral analysis
- **`polypersonaNoNation.py`** - Generates personas without nationality specifications for nationality-neutral analysis
- **`polypersonaNoPlace.py`** - Creates personas without place attachment for place-neutral analysis
- **`polypersonaNoPolitical.py`** - Generates personas without political ideology for political-neutral analysis
- **`polypersonaNoPVAttitude.py`** - Creates personas without PV system attitudes for PV-neutral analysis
- **`polypersonaNoPVownership.py`** - Generates personas without PV ownership for ownership-neutral analysis
- **`polypersonaO4mini.py`** - Creates personas optimized for GPT-4-mini model analysis
- **`polypersonaOrder.py`** - Generates personas with specific ordering preferences for sequence analysis
- **`polypersonaPlace1.py`** - Creates personas with place attachment level 1 for place sensitivity analysis
- **`polypersonaPlace7.py`** - Generates personas with place attachment level 7 for place sensitivity analysis
- **`polypersonaPolitical1.py`** - Creates personas with political ideology level 1 for political sensitivity analysis
- **`polypersonaPolitical10.py`** - Generates personas with political ideology level 10 for political sensitivity analysis
- **`polypersonaTemp0.3.py`** - Creates personas with temperature sensitivity 0.3 for climate sensitivity analysis
- **`polypersonaTemp0.7.py`** - Generates personas with temperature sensitivity 0.7 for climate sensitivity analysis
- **`polypersonaTemp1.2.py`** - Creates personas with temperature sensitivity 1.2 for climate sensitivity analysis
- **`polypersonaTemp2.0.py`** - Generates personas with temperature sensitivity 2.0 for climate sensitivity analysis
- **`polypersonaTrustFirst.py`** - Creates personas with trust-first decision-making patterns for trust analysis

### Test and Analysis Scripts

- **`testpolyexplan.py`** - Tests persona explanations and generates German replication data
- **`testpolyexplanUK.py`** - Tests persona explanations and generates UK replication data
- **`testpolyexplanUKGPT5mini.py`** - Tests persona explanations using GPT-5-mini model for UK data

### Data Processing and Analysis Scripts

- **`batch_reshape_to_long.py`** - Batch converts wide-format CSV files to long-format for statistical analysis
- **`reshape_data_wide.py` - Converts wide-format data to long-format (each persona from 1 row to 12 rows)
- **`reshape_data.py`** - Basic data reshaping utilities
- **`calculate_means.py`** - Calculates mean values across different demographic groups
- **`calculate_means_by_actor.py`** - Calculates means grouped by different actor types
- **`merge_replication_files.py`** - Merges multiple replication data files
- **`fix_csv.py`** - Fixes CSV formatting issues
- **`fix_csv_direct.py`** - Direct CSV fixing utilities
- **`fix_csv_final.py`** - Final CSV formatting corrections
- **`generate_histograms.py`** - Generates histogram visualizations of the data
- **`generate_histograms_simple.py`** - Simplified histogram generation

### Data Files

#### Demographic and Experimental Data
- **`demoprobs_fixed.csv`** - Fixed demographic probability distributions
- **`demoprobs.csv`** - Original demographic probability data
- **`condition0208.csv`** - Experimental condition settings
- **`condition0208trustFirst.csv`** - Trust-first experimental conditions
- **`conditions.csv`** - General experimental conditions

#### Generated Persona Data
- **`DE0308REPLICATION.csv`** - Main German replication dataset
- **`UK0308REPLICATION.csv`** - UK replication dataset
- **`DEreplication0708.csv`** - German replication data from July 8
- **`UKreplication0708.csv`** - UK replication data from July 8
- **`REPALL.csv`** - Combined replication dataset
- **`Sen*.csv`** - Various sensitivity analysis datasets (e.g., SenAgeYoung.csv, SenCC1.csv, etc.)

#### Analysis Results
- **`summary_comparison.csv`** - Summary comparison of different datasets
- **`Mean*.csv`** - Mean value calculations for different groups
- **`chart_data_*.csv`** - Chart data for various analyses

### Visualization and Output Files

#### Charts and Figures
- **`figure_*.png`** - Generated charts and visualizations for each sensitivity analysis
- **`Sen*_long_heatmap_*.png`** - Heatmap visualizations for long-format data analysis

#### Analysis Outputs
- **`out/`** - Output directory containing analysis results
  - **`dataset_scores.csv`** - Dataset performance scores and metrics
  - **`create_scatter_plot.py`** - Script for creating scatter plots of dataset scores
  - **`mixedlm_*.csv`** - Mixed linear model analysis results
  - **`metrics_by_cell.csv`** - Metrics calculated for different data cells

### R Analysis Scripts

- **`JSD.R`** - Jensen-Shannon Divergence analysis
- **`JSD2.R`** - Extended JSD analysis
- **`LMM.R`** - Linear Mixed Model analysis
- **`pic.R`** - Picture generation and visualization
- **`plot_all.R`** - Comprehensive plotting script for all analyses

## Key Features

1. **Comprehensive Persona Generation**: Creates virtual individuals with realistic demographic profiles
2. **Sensitivity Analysis**: Analyzes how different characteristics affect energy trading decisions
3. **Multi-Model Support**: Works with various GPT models (GPT-4, GPT-4-mini, GPT-5-mini)
4. **Statistical Analysis**: Includes comprehensive statistical analysis tools and visualizations
5. **Data Format Conversion**: Tools for converting between wide and long data formats
6. **Reproducible Research**: All scripts and data are included for reproducibility

## Usage

1. **Setup**: Install required Python packages (pandas, numpy, openai)
2. **Configuration**: Add your OpenAI API key to the persona generation scripts
3. **Generation**: Run the desired persona generation script
4. **Analysis**: Use the data processing and analysis scripts
5. **Visualization**: Generate charts and figures using the visualization scripts

## Data Structure

Each generated persona includes:
- **Demographics**: Age, gender, education, employment, household size
- **Energy Preferences**: Energy mix preferences, PV possession, investment intentions
- **Attitudes**: Political ideology, climate change attitudes, place attachment
- **Trading Preferences**: Sales and purchase preferences for different social groups
- **Trust Assessments**: Trust levels for various organizations and groups

## Output Formats

- **Wide Format**: Each persona as one row with multiple columns
- **Long Format**: Each persona expanded to multiple rows (12 per persona)
- **CSV Files**: All data exported in CSV format for easy analysis
- **Visualizations**: PNG charts and heatmaps for data exploration

## Research Applications

This framework is designed for:
- Energy trading behavior research
- Demographic sensitivity analysis
- Climate change attitude studies
- Political ideology impact analysis
- Trust and social preference research
- Peer-to-peer energy market analysis

## Security Note

⚠️ **Important**: All API keys have been removed from the scripts and replaced with placeholders. Please add your actual OpenAI API key before running the persona generation scripts.

## Citation

If you use this framework in your research, please cite the project appropriately.

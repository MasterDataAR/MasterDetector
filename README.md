# MasterDetector

Our study on anomaly detection with error repairing by master data in multivariate time series.

## Directory Structure

* `code/` includes the code for experiments (`src/main/java/`).
* `data/` includes the Trajectory dataset (`data/traj/`):

## Setup

1. **JDK**: Use JDK 1.17 or above (Java 8+ recommended).
2. **Build**: Package the project using Maven with the command:

   ```
   mvn clean install -U
   ```
3. **Run Experiments**: Execute `src/main/java/Experiment.java`. The main functions include:

   * `main_td_scale()` – results of varying time series data size.
   * `main_md_scale()` – results of varying master data size.
   * `main_error_rate()` – results of varying error rate.
   * `main_error_range()` – results of varying error range.
   * `main_error_length()` – results of varying error length.
   * `main_parameters(true, true, true, true)` – results of varying different parameters.
   * `whole_data_set(4)` – results on the whole dataset.
   * `varyingModel(5)` – results of varying different auto-regression models.

## Notes on Trajectory Dataset

* The dataset is located in `data/traj/`.
* `master_data_1180.csv` is the master data.
* `time_series_data_25168.csv` is the corresponding time series data.

## Deployment

The proposed methods have been deployed as a function in Apache IoTDB for anomaly detection with data repairing.

* [Introduction document](https://iotdb.apache.org/UserGuide/latest/SQL-Manual/UDF-Libraries_apache.html#masterdetect)
* [GitHub repository](https://github.com/apache/iotdb/tree/research/master-detector)

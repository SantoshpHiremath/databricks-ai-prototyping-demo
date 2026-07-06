# AI Prototyping — Databricks Demo Notebook

A hands-on Databricks notebook demonstrating core PySpark data exploration
and a basic MLlib machine learning workflow, built to gain practical,
verifiable exposure to the Databricks environment — directly matching job
postings that list "Databricks" as a required or preferred skill.

## Important honesty note

This notebook gives me real, hands-on exposure to the Databricks notebook
environment (Free/Community Edition) — not production or enterprise
experience (clusters at scale, Delta Lake, job orchestration, team
workflows). I'm upfront about that distinction: I describe this as
"hands-on exposure to the Databricks notebook environment and PySpark
basics," not "Databricks experience." If asked a follow-up question that
goes beyond what I actually did, my honest answer is: "I've only used the
free tier for a personal notebook so far, but I understand the core
workflow and I'm ready to learn the production side quickly."

## What this demonstrates

- Loading and inspecting a real sample dataset (`adult.data`, the UCI
  Adult Census Income dataset) using PySpark's `spark.read.csv`
- Renaming raw, auto-generated columns for clarity and inspecting the
  schema with `printSchema()`
- Basic DataFrame operations: filtering rows by condition and
  aggregating with `groupBy` + `avg`
- A full, correctly-evaluated MLlib pipeline: feature assembly with
  `VectorAssembler`, a train/test split, fitting a `LinearRegression`
  model, and evaluating it with RMSE and R² on held-out test data
- Honest interpretation of a real result: the model's R² was low
  (~0.03), and rather than hide that, the notebook explicitly explains
  why (age and education alone don't strongly predict hours worked) —
  showing I can read and reason about model output, not just run code

## Files

- `AI-Prototyping-Databricks-Demo.ipynb` — the full notebook, exported
  directly from Databricks with all code and output preserved. Renders
  on GitHub with both code and results visible.

## Tech used

Databricks (Free/Community Edition), PySpark (DataFrame API, MLlib —
`VectorAssembler`, `LinearRegression`), Python.
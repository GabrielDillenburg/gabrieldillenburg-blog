---
title: "Performance of OpenMP Applications in HPC Environments: A Detailed Approach with Task Tracking"
description: An in-depth exploration of optimizing OpenMP applications for High-Performance Computing through task tracking
slug: openmp-hpc-performance
date: 2024-04-10T10:00:00-03:00
categories:
    - High-Performance Computing
    - Parallel Programming
    - Applications Performance
tags:
    - HPC
    - OpenMP
    - Performance Optimization
    - Task Tracking
image: 
math: true
license: 
comments: true
draft: false
---

This document presents a proposal for my research project, which is a pivotal component of my master's degree in computer science at the Federal University of Rio Grande do Sul. The focus of this study is on optimizing OpenMP applications within High-Performance Computing (HPC) environments, with a particular emphasis on the critical role of task tracking. Under the supervision of Prof. Dr. Lucas Mello Schnorr, this project aims to outline effective methodologies, engage in comprehensive case studies, and conduct a comparative analysis on the performance of OpenMP task directives.

## Introduction

In the realm of HPC, addressing complex problems necessitates substantial computational power. This research proposal is dedicated to enhancing the performance of OpenMP applications by leveraging task tracking methodologies. It seeks to provide insights into the nuances of parallel programming and the adaptability required in the multi-core processor environments characteristic of modern HPC systems.

## Objectives

The principal aim of this research project is to develop a methodology for tracking OpenMP task directives. This will enable us to identify performance bottlenecks in parallel applications accurately. Utilizing the OMPT interface for detailed data collection on task execution, we aspire to deepen our understanding of how tasks are executed and interact within applications, facilitating improved performance optimization strategies.

## Related Work

Our investigation builds upon seminal studies focused on optimizing and evaluating OpenMP parallel processing within HPC environments. These studies lay the groundwork for our exploration into effective task synchronization and achieving higher computational efficiencies.

## Methodology

We propose a methodology that blends benchmark analysis with thorough performance evaluations across various hardware configurations. Employing the KASTORS suite for our case studies, we will examine the impact of task granularity and execution efficiency in a diverse array of HPC settings.

## Case Studies: KASTORS Benchmarks

The project will leverage benchmarks such as Jacobi, Plasma, Sparselu, and Strassen from the KASTORS suite. These are designed to explore the challenges and opportunities of task-based parallelism and optimizations within OpenMP 4.0 and subsequent versions.

## HPC Simulation Platforms at UFRGS

Our simulations will be conducted across distinct platforms within the [High-Performance Computing Park](https://gppd-hpc.inf.ufrgs.br/) at UFRGS. From the 24-core Cei to the 44-core Blaise, these platforms offer a range of computational capabilities, allowing us to assess the impact of different hardware configurations on application performance.

## Research Timeline

The research timeline extends from April to July 2024, beginning with a comprehensive literature review and progressing through benchmark testing on selected hardware configurations. The project will culminate in the analysis of our findings and the dissemination of our research results.

For a more detailed view, you can access the full study in the embedded PDF below.

<iframe src="/pdfs/ppgc-rp.pdf" style="width: 100%; height: 500px; border: none;"></iframe>

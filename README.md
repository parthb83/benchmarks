# Google Summer of Code 2022 with CVXPY (NumFOCUS)
This is the final work submission for my Google Summer of Code (GSoc) participation with CVXPY, a suborganization of NumFOCUS. My work during GSoC period revolved around benchmarking the CVXPY repository with a tool called `Airspeed Velocity` and also to inform the maintainers about potential regressions introduced to the codebase for each Pull Request. This report summarizes my experience contributing to CVXPY during this period.

## Pre-GSoC Period
The PRs I made during the Pre-GSoC period are:
- [#1641](https://github.com/cvxpy/cvxpy/pull/1641): Added new atom function xexp()
- [#1683](https://github.com/cvxpy/cvxpy/pull/1683): Updated cumsum test, added cummax test, fix cummmax
- [#1768](https://github.com/cvxpy/cvxpy/pull/1768): Add condition_number as a quasi-convex atom

These PRs helped me in understanding the CVXPY codebase as well as the concept of Convex Optimization greatly. Contribution during this period also helped in connecting to the CVXPY community and communicating with the CVXPY project maintainers and developers like Steven Diamond, Riley Murray, and Philipp Schiele.

## Community Bonding Period
After my [Proposal for the Benchmarking Project](https://drive.google.com/file/d/1be94687ztzGv3OUvf5EkoyljEpGY1uCB/view?usp=sharing) was accepted, I spent this time in getting to know the concept of benchmarking as well as discussing with my GSoC mentor, Philipp Schiele, the roadmap for the coding period and the goals that are to be achieved with this project. The major PR that I made during this period was:
- [#4](https://github.com/cvxpy/benchmarks/pull/4): First working draft of Airspeed Velocity

This PR was made to migrate the demo benchmarking setup made by the project maintainers, to the one that was using **Airspeed Velocity**, a tool that is used to benchmark python repositories conveniently over their lifecycle.

## Coding Period
### Pre-Midtrem Evaluation
This was one of the most important parts of the whole project. I had to create separate workflows in **Github Actions** for benchmarking each PR and commenting the results under the same PR so that it is easy for the project maintainers to see if the new addition to the codebase would introduce some performance regressions or not. The `HEAD` commit of the PR and the `origin/master` commit of the original codebase are benchmarked (importantly: on the same machine) and the results are compared to check for any regressions. The PRs I made during this period were:
- [#1798](https://github.com/cvxpy/cvxpy/pull/1798): Added benchmarks workflow to benchmark the master branch of cvxpy and upload results
- [#1810](https://github.com/cvxpy/cvxpy/pull/1810): New workflow to make benchmarks to run on PR commits

The final results after merging the PR were published in HTML and hosted on **Github Pages**: [Link to page](https://cvxpy.github.io/benchmarks/).

### Post-Midterm Evaluation
This period was used to add new benchmarks to the benchmarking suite of the repository. Some benchmarks added by me were:
- [#7](https://github.com/cvxpy/benchmarks/pull/7): **Optimal Advertising**
- [#8](https://github.com/cvxpy/benchmarks/pull/8): **SVM with L1 Regularization**
- [#9](https://github.com/cvxpy/benchmarks/pull/9): **Huber Regression**
- [#10](https://github.com/cvxpy/benchmarks/pull/10): **Semidefinite Programming**
- [#11](https://github.com/cvxpy/benchmarks/pull/11): **Factor Covariance Model and Gini Portfolio Optimization**

These problems were selected to cover a wide variety of fields in which Convex Optimization is used and to also benchmark a substantial portion of the CVXPY codebase.

## Experience and future plans
Working with the CVXPY community was a great learning experience. CVXPY community is really helpful for anyone stuck at any phase of development. Working with my mentors and administrators I learned how to write clean and maintainable code. Thanks to Philipp for always being available whenever I had some problems and holding regular Zoom calls for reviewing my work, clearing my doubts, and discussing further plans about the project. I would like to contribute to CVXPY even after GSoC in domains other than benchmarking too as I've learned a lot of things while working with the CVXPY community and wish to contribute and continue this journey even further.

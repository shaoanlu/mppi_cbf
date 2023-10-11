# mppi_cbf_playground
Colab notebooks of personal experiments with MPPI and CBF.

### Contents
1. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaoanlu/mppi_cbf_playground/blob/main/bicycle_mppi_cbf_shielding.ipynb) MPPI with CBF for trajectory planning
<p align="center">
  <img src="mppi_anim.gif" width=400>
</p>


### Note for implementations
- Terminal cost of MPPI is non-trivial. It improves the quality of prior of control sequence and therefore prevent the controller to unnecessaryly drive the system away from target position.
- Discrete CBF cost is a good fit to sampling based predictive controllers and only introduces little extra computation
- Gaurantee of CBF-QP is lost with discretization.

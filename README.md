# mppi_cbf_playground
Colab notebooks of personal experiments with MPPI and CBF.

### Contents
1. MPPI for trajectory planning and obstacle avoidance [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaoanlu/mppi_cbf_playground/blob/main/bicycle_mppi_cbf_shielding.ipynb)
    - With safety gaurantee from 1) CBF constraint, 2) CBF-QP safety filter, and 3) nonlinnear predictive filter[1]
<p align="center">
  <img src="mppi_anim.gif" width=400>
</p>


### Note for implementations
- The terminal cost in MPPI is significant. It enhances the quality of the control sequence's prior, thereby preventing the controller from inadvertently deviating the system from its target position.
- The discrete CBF cost aligns well with sampling-based predictive controllers, introducing only minimal additional computation.
- The guarantees provided by CBF-QP diminish with discretization.


### References
1. Shield Model Predictive Path Integral: A Computationally Efficient Robust MPC Approach Using Control Barrier Functions, Ji Yin, et.al. https://arxiv.org/abs/2302.11719

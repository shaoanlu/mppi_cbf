# mppi_cbf_playground
Colab notebooks of personal experiments with MPPI and CBF.

### Contents
1. MPPI trajectory planning and obstacle avoidance [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaoanlu/mppi_cbf_playground/blob/main/bicycle_mppi_cbf_shielding.ipynb)
    - Safety gaurantee based on 1) CBF, 2) CBF-QP, and 3) nonlinnear predictive filter
<p align="center">
  <img src="mppi_anim.gif" width=400>
</p>


### Note for implementations
- The terminal cost in MPPI is significant. It enhances the quality of the control sequence's prior, thereby preventing the controller from inadvertently deviating the system from its target position.
- The discrete CBF cost aligns well with sampling-based predictive controllers, introducing only minimal additional computation.
- The guarantees provided by CBF-QP diminish with discretization.

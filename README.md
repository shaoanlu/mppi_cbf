# mppi_cbf_playground
Colab notebooks of personal experiments with MPPI and CBF.

## Content


| Nominal Controller | Safety Filter               | Model                                   | Colab Link                                                                                                                                                                                             |
| ------------------ | --------------------------- | --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| MPPI               | CBF cost                    | Bicycle car                             | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaoanlu/mppi_cbf_playground/blob/main/bicycle_mppi_cbf_shielding.ipynb)         |
|                    | CBF-QP                      | Bicycle car                             | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaoanlu/mppi_cbf_playground/blob/main/bicycle_mppi_cbf_shielding.ipynb)         |
|                    | Nonlinear predictive filter | Bicycle car                             | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaoanlu/mppi_cbf_playground/blob/main/bicycle_mppi_cbf_shielding.ipynb)         |
| MPPI               | CBF cost                    | Planar quadrotor                        | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaoanlu/mppi_cbf_playground/blob/main/planar_quadrotor_mppi_cbf.ipynb)          |
| MPPI               | CBF cost                    | Planar quadrotor with suspended payload | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shaoanlu/mppi_cbf_playground/blob/main/planar_quadrotor_pendulum_mppi_cbf.ipynb) |

## Demonstrations
### Demo 1: bicycle car
The following animations are simulation result of MPPI controller for obstacle avoidance.
- Left: w/ CBF as a cost term in MPPI.
- Middle: w/ a CBFQP safety filter.
- Right: w/ a nonlinear predictive safety filter.
<p align="center">
  <img src="assets/bicycle_mppi_cbf_anim.gif" width=250> <img src="assets/bicycle_mppi_cbfqp_anim.gif" width=250> <img src="assets/bicycle_mppi_shielding_anim.gif" width=250>
</p>

### Demo 2: planar quadrotor
The following animations are simulation result of MPPI controller with CBF cost for obstacle avoidance.
<p align="center">
  <img src="assets/2Dquadrotor_mppi_cbf_anim.gif" width=250> <img src="assets/2Dquadrotor_pendulum_mppi_cbf_anim.gif" width=250>
</p>


### Note for implementations
- The terminal cost in MPPI is significant. It enhances the quality of the control sequence's prior, thereby preventing the controller from inadvertently deviating the system from its target position.
- The discrete CBF cost aligns well with sampling-based predictive controllers, introducing only minimal additional computation.
- The guarantees provided by CBF-QP diminish with discretization.


### References
1. Yin, Ji, et al. "Shield Model Predictive Path Integral: A Computationally Efficient Robust MPC Approach Using Control Barrier Functions." arXiv preprint arXiv:2302.11719 (2023). https://arxiv.org/abs/2302.11719
2. Ames, Aaron D., et al. "Control barrier functions: Theory and applications." 2019 18th European control conference (ECC). IEEE, 2019. https://arxiv.org/abs/1903.11199

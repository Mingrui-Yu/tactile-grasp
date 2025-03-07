---
layout: default
---

<script type="text/javascript" async
  src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.2/es5/tex-mml-chtml.js"></script>
<script type="text/javascript">
  MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']]
    }
  };
</script>

# Minimizing Undesired Object Movements in Dexterous Grasping Control with Tactile-Feedback Arm-Hand Coordination

<p style="text-align: center;"> 
<a href="https://mingrui-yu.github.io/tactile-grasp/" style="color: #0ABAB5; text-decoration: underline;">arXiv (comming soon)</a> |
<a href="https://github.com/Mingrui-Yu/tactile-grasp" style="color: #0ABAB5; text-decoration: underline;">Code (comming soon)</a>
</p>

The paper has been submitted to IROS 2025.

## Video

<video controls style="width: 100%; height: auto;">
    <source src="./final.mp4" type="video/mp4">
</video>

## Abstract

While dexterous grasp pose generation has been widely studied recently, less attention has been given to the actual execution of planned grasps. Owing to object position and shape uncertainties, open-loop executions of the planned grasps usually result in uncoordinated contacts on the object, leading to undesired in-hand object movements and even grasp failures.
This work addresses the gap by proposing an optimization-based tactile-feedback grasping control framework to minimize undesired object movements during the execution of a planned grasp.
Our framework consists of three stages: global approaching, contact establishment, and grasp force exertion, with a emphasis on coordinated forces across multiple fingers to ensure a gentle grasping. Unlike existing works, our approaches focuses on the whole-process grasping control, during which both the arm and hand motions are optimized to improve grasp quality.
Real-world experiments demonstrate that the proposed approach significantly reduces undesired in-hand object movements and maintains wrench balances in the presence of visual perception errors and imperfect planned grasp poses.

## Appendix

### Hyper-Parameters

- Stage 1:
  - \\(l = 0.04\\)
  - \\(\lambda\_{1, q} = 0.001\\)
- Stage 2:
  - \\(\gamma = 1.0\\)
  - \\(\lambda\_{2, \rm f} = 1.0\\)
  - \\(\lambda\_{2, \rm a} = 1.0\\)
  - \\(q\_{\rm vel, max}^{af} = [..., 0.2, ...] \text{(rad)} \\)
- Stage 3:
  - \\(K_e = \text{diag}(10^6, 10^6, 700)\\). Note that we assign large values for the tangential dimensions to penalize tangential motions.
  - \\(K_p = \text{diag}(0.01, 0.01, 0.01, 0.01)\\)
  - \\(\lambda\_{3, q} = 1.0\\)
  - \\(\mu = 0.1\\)
  - \\(f^{\rm thumb}\_{\rm g, max} = 1.5 \text{(N)} \\)
  - \\(q\_{\rm vel, max}^{f} = [..., 0.1, ...] \text{(rad)} \\)

## Contact

If you have any question, feel free to contact the authors: Mingrui Yu, [mingruiyu98@gmail.com](mailto:mingruiyu98@gmail.com) .

Mingrui Yu's Homepage is at [mingrui-yu.github.io](https://mingrui-yu.github.io).

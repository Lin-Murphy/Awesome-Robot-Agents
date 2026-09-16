# Awesome Robot Agents — Embodied AI & Robot Manipulation

**A source-aware directory of embodied AI agents for robotic manipulation.** It tracks GPT-6 Astra and other LLM/VLM systems across robot arms, grasping, simulation, and real-world demonstrations, with links to their decisions, execution interfaces, available code, and supporting evidence. As GPT-6 Astra brings renewed attention to this direction, the collection follows how the field develops across models and arms.

## Contents

- [Robot-arm projects](#robot-arm-projects)
- [Tools and evaluation](#tools-and-evaluation)
- [Further reading](#further-reading)
- [Original demonstrations](#original-demonstrations)
- [Contribute](#contribute)

## What this collection covers

An embodied-AI agent adds a reasoning and tool-use layer to the robot-control stack. An LLM/VLM may interpret a task, choose robot skills, and delegate precise motion to a low-level controller or policy. This differs from an end-to-end policy or VLA that maps observations directly to actions.

Entries identify the robot or simulator, execution interface, available code or demonstrations, and important evidence limits. Results remain author-reported unless a documented maintainer rerun is available.

## Robot-arm projects

### Robocurve Astra arm comparison

GPT-6 Astra plans and calls motion skills through Inspect Robots on real YAM arms. The [report and trial records](https://openai.robocurve.org/gpt-6-astra/) describe a two-task comparison with Claude models. The authors report 19/20 bowl-task completions and 2/20 puzzle-task completions for Astra; these tasks do not establish general robot competence.

**Source:** [Report and trial records](https://openai.robocurve.org/gpt-6-astra/) · [Video](https://openai.robocurve.org/gpt-6-astra/video/bowl-astra-vs-fable51-cost.mp4)

<p align="center"><a href="https://openai.robocurve.org/gpt-6-astra/video/bowl-astra-vs-fable51-cost.mp4"><img src="assets/robocurve-astra.gif" alt="Robocurve Astra bowl-task GIF preview" width="820"></a></p>

### GPT-Policy-Eval

An author-reported real-robot preview of GPT-6 Astra using a demonstration video and live visual feedback for plug insertion. The [project and videos](https://github.com/cheng-haha/GPT-Policy-Eval) are public; code and systematic evaluation are still planned. The checked README does not specify the robot model or exact action interface.

**Source:** [Project](https://github.com/cheng-haha/GPT-Policy-Eval) · [Video](https://github.com/cheng-haha/GPT-Policy-Eval/raw/refs/heads/main/assets/plug-insertion-top-and-right-wrist.mp4)

<p align="center"><a href="https://github.com/cheng-haha/GPT-Policy-Eval/raw/refs/heads/main/assets/plug-insertion-top-and-right-wrist.mp4"><img src="assets/gpt-policy-eval.gif" alt="GPT-Policy-Eval plug-insertion GIF preview" width="820"></a></p>

### Show-Harness

A released, model-flexible VLM harness for robot-arm manipulation. The VLM selects bounded action units; robot-specific interpreters turn them into motion for Franka or Piper arms, or for supported simulators. The authors provide [code, setup guides, and model/data links](https://github.com/showlab/Show-Harness). A public run guide is a starting point, not a maintainer-verified hardware result.

**Source:** [Project and code](https://github.com/showlab/Show-Harness)

<p align="center"><a href="https://github.com/showlab/Show-Harness"><img src="assets/show-harness.png" alt="Show-Harness: the VLM thinks and the robot moves" width="820"></a></p>

### Pigey — Physical Agency

A closed-loop VLM orchestrator that routes high-level reasoning through frozen robot skills. The project reports LIBERO-PRO simulation results and Franka FR3 real-robot tasks, with code and a paper linked from the project page.

**Source:** [Project and demos](https://lianegalanti.github.io/Pigey/)

<p align="center"><a href="https://lianegalanti.github.io/Pigey/"><img src="assets/pigey-scene-memory.png" alt="Pigey scene-memory demonstration: memorize five dolls, look away during a shuffle, then restore their original positions" width="820"></a></p>

*Project-page screenshot supplied by the contributor. [Author-reported demonstration](https://lianegalanti.github.io/Pigey/): remember five dolls’ positions, look away while they are shuffled, then restore the scene using the stored positions.*

### ENPIRE

An open agentic framework for coding agents to improve real-world robot policies through repeated reset, execution, verification, recording, and refinement. It provides hardware-free examples plus workflows for calibrated physical stations; real-robot use requires the project's own safety and authorization preflight.

**Source:** [Repository](https://github.com/NVlabs/ENPIRE)

<p align="center"><a href="https://github.com/NVlabs/ENPIRE"><img src="assets/enpire-workflow.png" alt="ENPIRE workflow: coding agent, tool APIs, environment, and policy improvement" width="820"></a></p>

## Tools and evaluation

Tools for connecting or evaluating robot agents.

- [Inspect Robots](https://github.com/robocurve/inspect-robots) — connects an agent or policy to a robot, task, and run logs. Its mock quick start checks the pipeline, not physical manipulation; see the [LLM-agent guide](https://github.com/robocurve/inspect-robots#drive-the-robot-with-an-llm).
- [ROS MCP Server](https://github.com/robotmcp/ros-mcp-server) — exposes ROS topics, services, and actions to an MCP client. It provides an interface, not the robot controller itself.
- [StationeryBench](https://github.com/robocurve/stationerybench) — a benchmark and scoring protocol for bimanual stationery tasks. Its scripted mock is not a robot success result.
- [FluxVLA](https://github.com/FluxVLA/FluxVLA) — a VLA platform for simulation and real-robot deployment. Here it is the low-level policy/backend associated with the Jikun lead, not the LLM agent itself.

## Further reading

- [OpenAI: GPT-6 Astra](https://openai.com/index/gpt-6-astra/) — the original announcement and system overview.
- [Robot-Use Agents](https://web.mit.edu/phillipi/www/writing/robot-use-agents.html) — a perspective on using language models as tools for robots, including the distinction between high-level reasoning and low-level control.
- [Awesome Robot Use Agent](https://github.com/kairunwen/Awesome-Robot-Use-Agent) — a broader catalogue of robot-use-agent papers, projects, benchmarks, and community demonstrations; useful as a discovery index alongside this robot-arm-focused collection.

## Original demonstrations

Author-created demonstrations; code and technical details are linked when available.

| Media | Source | Reported task |
| --- | --- | --- |
| <a href="https://x.com/DJiafei/status/2096601096705995155"><img src="assets/gpt6-astra-gripper.png" alt="GPT-6 Astra gripper alignment" width="420"></a> | Jiafei Duan — [Original post](https://x.com/DJiafei/status/2096601096705995155)<br>[MolmoAct2 sim_eval](https://github.com/allenai/molmoact2/tree/main/sim_eval) | Tabletop grasp and place in simulation |
| <a href="https://x.com/RotekSong/status/2099104628562608371"><img src="assets/roteksong-g1-cola.png" alt="RotekSong G1 cola bottle pick-up" width="420"></a> | RotekSong — [Original post](https://x.com/RotekSong/status/2099104628562608371) | G1 cola-bottle pick-up in Isaac Sim |
| <a href="https://x.com/kaiwynd/status/2098823484474348008"><img src="assets/kaifeng-keyboard.png" alt="Kaifeng Zhang Astra keyboard interaction" width="420"></a> | Kaifeng Zhang — [Original post](https://x.com/kaiwynd/status/2098823484474348008) | Real-robot keyboard interaction with visual feedback; Astra learns to type after repeated attempts |
| <img src="assets/star-marker-grasp.png" alt="star大小变 robot-arm gripper holding a red marker" width="420"> | star大小变 — [Original post](https://www.rednote.com/discovery/item/6aa4d7e200000000260145ff?source=web_profile_page&xsec_source=pc_search&xsec_token=ABur_B60E14GxVQp2ei3USGtEElW40SN75Vj5aB_USVUA%3D) | Low-level robot-arm marker grasp |
| <img src="assets/axel-mobile-manipulation.png" alt="Axel mobile manipulation" width="420"> | Axel — [Original post](https://x.com/ax_pey/status/2098216469012283681)<br>[Code PR](https://github.com/innate-inc/innate-os/pull/817) | Video-based in-context learning for mobile manipulation across environments, camera views, and layouts; Astra chooses end-effector or joint-space control without a text prompt |
| <img src="assets/lucas-adaptation.png" alt="Lucas Cassiano robot adaptation" width="420"> | Lucas Cassiano — [Original post](https://x.com/lucascassiano/status/2097830777438486557) | Rapid adaptation to an unseen robot embodiment |
| <img src="assets/tonghe-harness.png" alt="Tonghe Zhang robot harness" width="420"> | Tonghe Zhang — [Original post](https://x.com/TongheZhang01/status/2097801107602911243)<br>[ENPIRE](https://github.com/NVlabs/ENPIRE) | Robot in-context learning through the ENPIRE harness |
| <img src="assets/thijs-painting.png" alt="thijs robot-arm painting demonstration, Attempt 02" width="420"> | thijs — [Original post](https://x.com/cdngdev/status/2097339677128982873) | Painting task from a semantic prompt |
| <img src="assets/jikun-simulation.png" alt="Jikun robot-arm simulation with external and wrist-camera views" width="420"> | Jikun — [Original post](https://www.rednote.com/discovery/item/6aa16835000000000b00f46d?source=web_profile_page&xsec_source=pc_search&xsec_token=ABDcu5eBZZYkAUcveAv8IZNWsbLmXk6CUM5u5BhDPODB0%3D)<br>[FluxVLA](https://github.com/FluxVLA/FluxVLA) | Astra planning with a pretrained embodied policy |
| <img src="assets/loopros-cucumber.png" alt="Loop-ROS cucumber cutting" width="420"> | 盒子桥 — [Original post](https://www.rednote.com/discovery/item/6aa0c4900000000012034a2f?source=webshare&xhsshare=pc_web&xsec_token=ABYB6HItIwwYq0Yyi9-hwoM-vMalkFRmYMAkN0iUWpTM4=&xsec_source=pc_share)<br>[LoopMaster](https://loopmaster.ai/) | Real-arm cucumber slicing through Loop-ROS |
| <img src="assets/yingwu-astra-real2sim.png" alt="Astra video reconstruction and robot-arm control" width="420"> | 应物而无累 — <a href="https://www.rednote.com/discovery/item/6aa8985a000000002a02f022?source=webshare&xhsshare=pc_web&xsec_token=ABVaBndlmLfLukTWqmYV_Z_deDleX-ebQ1EIyqCo1cfy4=&xsec_source=pc_share">Original post</a> | Video-to-simulation asset reconstruction followed by robot-arm control |
| <img src="assets/droid-closed-loop.png" alt="DROID GPT visual closed loop" width="420"> | Loule — <a href="https://www.rednote.com/discovery/item/6a9fc0710000000029015578?source=webshare&xhsshare=pc_web&xsec_token=ABMaVBcBS54ctuQIxmhMJMZSAU7Wspgd3bmCnb4tQqHsU=&xsec_source=pc_share">Original post</a> | Real-arm bread pick and place using end-effector poses |
| <img src="assets/multi-arm-lab.png" alt="Multiple robot arms" width="420"> | 虽然不但是 — <a href="https://www.rednote.com/discovery/item/6a9bd4c80000000028037f67?source=webshare&xhsshare=pc_web&xsec_token=ABLUcokp8Tzdy13Avv1khxst1pWqWBaR7JLjQhUhWsSs4=&xsec_source=pc_share">Original post</a> | Piper pick and place with GPT-6 and RealSense |
| [Interactive demo](https://qinengwang-aiden.github.io/demos/constraint_demos/) | Qineng Wang — [Original post](https://x.com/qineng_wang/status/2099893504658866561)<br>[Methods and evidence](https://qinengwang-aiden.github.io/demos/constraint_demos/methods.html) | GPT-6 Astra spatial-constraint demonstrations: unlocking interlocked parts and threading a rope through three rings in Dual ALOHA simulation/replay; author-reported demonstration, not physical-hardware validation |

Demonstrations can be expanded into full entries when supporting code or technical details become available.

## Contribute

Suggest a project related to **LLM/VLM agent participation in robot-arm manipulation** through an [issue](https://github.com/Lin-Murphy/Awesome-Robot-Agents/issues) or the [contribution instructions](CONTRIBUTING.md). Include the model's decision, execution interface, robot or simulator, available code or demos, and key evidence limits.

## Attribution and license

The [MIT license](LICENSE) covers this collection's original text and templates only. Linked code, data, media, and trademarks remain subject to their original terms. Entries are source-based and author-reported, not endorsements or maintainer-verified hardware results. This is an independent collection, unaffiliated with listed projects or providers.

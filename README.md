### Hi, I'm Joseph 👋

You know the feeling: you change one line, rerun the benchmark, and the FPS counter jumps. That's the best part of my day, and it's why my Intel Arc B580 rarely gets to rest.

Most of what's here started as *"I wonder if this model can run locally"* and turned into *"okay, one more profiling run."* OpenVINO, NNCF, quantization, moving work onto the GPU, watching the latency drop. That loop never gets old.

[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-light434-FFD21E?logo=huggingface&logoColor=black)](https://huggingface.co/light434)
[![Email](https://img.shields.io/badge/Email-josephbabu308%40gmail.com-informational?logo=gmail&logoColor=white)](mailto:josephbabu308@gmail.com)

---

#### ⚡ Things that kept me up

**[ATHENA](https://github.com/ligth279/ATHENA)**: an offline AI tutor, four models, one 12 GB GPU.
Llama 3.1 8B, Whisper, TranslateGemma and OmniVoice take turns on the Arc through OpenVINO. Each model loads, does its job, and gets out of the way, and GPU memory goes back to zero between hops. Getting that handoff clean was the fun part.

**[whoami / perception](https://github.com/ligth279/whoami/tree/dev1-turing-perception/turing)**: helping an outdoor robot see (team project, I own perception).
SegFormer-B5 segmentation plus metric depth on OpenVINO GPU, wired into ROS 2. Taking it from **2.15 to 13.2 FPS**, one optimization at a time, was one of the most fun stretches I've had: moving pre- and post-processing onto the GPU, splitting depth into its own worker, and watching mask latency fall from **~415 ms to 61.2 ms**.

**[translategemma-4b-it-int8-ov](https://huggingface.co/light434/translategemma-4b-it-int8-ov)**: a 4B translator, squeezed to INT8 with NNCF.
Runs on Arc through OpenVINO GenAI and still holds **BLEU 34.83 / chrF 62.1** (WMT24++ en→es subset). Shared so nobody else has to redo the export.

**[OmniVoice-0.2.1-fp16-ov](https://huggingface.co/light434/OmniVoice-0.2.1-fp16-ov)**: text-to-speech on Intel GPU, no PyTorch at runtime.
**1.69% WER** across all 1088 Seed-TTS English lines, at a real-time factor of **0.094**. I also tried a GPU-side CFG and benchmarked it against the main path. It came out 2.5× slower, so it stays experimental, and a fused version is next.

**[Xilo AI Tutor v5](https://github.com/ligth279/xilov5-overhual)**: where the rabbit hole began.
GPT-OSS 20B on a consumer GPU via llama.cpp + Vulkan, teaching in 13 languages at 3.7–7.0 tok/s.

**[coHerence](https://github.com/ligth279/coHerence)**: asking *who* software fails for, not just whether it works (team project).
Built the deterministic fairness scoring, LLM diagnosis, FastAPI gateway and pipeline.

---

**🧰 Usual toolbox:** OpenVINO · OpenVINO GenAI · NNCF · INT8/INT4 · Optimum-Intel · PyTorch · llama.cpp · Vulkan · ROS 2 · Python · FastAPI · Linux

**🔭 Looking for:** a 2027 internship with people who also get a little too happy about a 10 ms win.

B.Tech CSE · Kerala, India · 📫 josephbabu308@gmail.com

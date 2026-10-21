# Activity Chain Generator

[Demo](https://umn-choi-lab.github.io/activity-chains/) for the persona-as-rationale distillation paper (Feng, Yoon, Woo, Choi), under review at Transportation Research Part C.

`index.html`: precomputed gallery using Qwen3.5-2B Arm B QLoRA students (teacher Qwen3.5-27B) for 4 regions:

- Minneapolis-Saint Paul, Metropolitan Council Travel Behavior Inventory 2023
- England, National Travel Survey 2023
- the Netherlands, ODiN 2023
- Greater Melbourne, VISTA 2023-24

Profiles are synthetic grids, with no real respondent record or observed day. Generation uses 3 samples per profile, temperature 0.8, top-p 0.92. Schema-invalid generations are dropped; nothing else is filtered.

`live.html` retains the June 2026 in-browser WebGPU build with earlier Qwen2.5-1.5B students for Minneapolis-St. Paul and Seoul, with a note. The 2B students have no browser build yet.

Gallery data (`data/web_demo_{msp,england,netherlands,melbourne}.json`) comes from `scripts/demo/` in the private persona-rationale lab repo. Adapters are in [private UMN-Choi-Lab repositories](https://huggingface.co/UMN-Choi-Lab).

Survey microdata is never published. Outputs are synthetic and for research illustration only.

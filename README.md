# Cadence-content-pipeline
Based on the structure and contents visible in the [will-kelly/Cadence-content-pipeline](https://github.com/will-kelly/Cadence-content-pipeline) repository, here is an overview of its design and workflow:

**Primary Purpose**
The **Cadence Content Pipeline** is a structured, prompt-driven content generation framework built specifically for **Claude**. It standardizes the end-to-end process of intaking, drafting, filtering, and distributing marketing or brand content across multiple channels while maintaining a consistent voice and human-like quality.

**How the Pipeline Functions**
The system processes raw inputs into finished channel-specific deliverables using modular Markdown templates:

1. **Intake (`03_INTAKE_TEMPLATE.md`):** Captures topic requirements, target audience, primary goals, and baseline context.
2. **Voice & System Persona (`01_AGENT_PROFILE.md`, `02_SYSTEM_PROMPT.md`, `04_VOICE_LIBRARY.md`):** Configures Claude with specific tone guidelines, agent behavior rules, and stylistic constraints.
3. **Drafting & Multi-Channel Specs (`06_CHANNEL_SPECS.md`):** Generates content tailored for various target platforms (e.g., social media, email, blogs) following platform-specific constraints.
4. **Quality Control (`05_AI_TELL_FILTER.md`):** Applies a specialized filter to detect and strip out common AI clichés, repetitive phrasing, and synthetic voice artifacts.
5. **Scheduling & Execution (`07_CALENDAR_TEMPLATE.md`, `08_HANDLER_PLAYBOOK.md`):** Maps content to an execution schedule and provides operational playbooks for review, publication, and workflow handling.

**Key Technologies & Integration Methods**

* **Primary AI Engine:** Anthropic's Claude.
* **Format:** Modular Markdown (`.md`) files designed to be loaded directly into Claude Projects, API prompts, or custom system instructions.
* **Distribution Package:** Includes a packaged release file (`cadence-agentalent-submission.zip`) for standalone deployment or submission.

**Implementation Workflow**
To use this pipeline in your workflow:

1. **Setup:** Upload or paste `01_AGENT_PROFILE.md`, `02_SYSTEM_PROMPT.md`, `04_VOICE_LIBRARY.md`, and `05_AI_TELL_FILTER.md` into a **Claude Project** or system prompt context.
2. **Input:** Fill out `03_INTAKE_TEMPLATE.md` with your specific topic or campaign details and feed it into Claude.
3. **Generation & Filtering:** Allow Claude to draft campaign assets according to `06_CHANNEL_SPECS.md`, while automatically enforcing the AI-tell filter to ensure natural-sounding output.
4. **Execution:** Review output using the `08_HANDLER_PLAYBOOK.md` guidance and schedule content using `07_CALENDAR_TEMPLATE.md`.

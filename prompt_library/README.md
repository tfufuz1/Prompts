# Prompt Library for Advanced AI Interaction

Welcome to the Prompt Library! This collection offers a range of versatile and structured prompts designed to facilitate sophisticated interactions with Large Language Models (LLMs) and other AI systems. The prompts are inspired by an analysis of advanced prompt engineering techniques and aim to provide robust templates for various tasks, from content generation to complex reasoning.

## Directory Structure

This library is organized into the following categories:

*   **`meta_prompts/`**: Contains prompts designed to help you create or refine other prompts.
    *   `meta_prompt_framework_generator.md`: Helps generate a new, detailed prompt framework for a specific AI role or task.
    *   `prompt_optimizer.md`: Helps refine and optimize an existing prompt for better clarity and effectiveness.
*   **`interactive_dialogue/`**: Holds prompts that establish structured, multi-turn conversations with an AI.
    *   `interactive_dialogue_options.md`: Sets up a dialogue where the AI offers numbered options to guide the user.
    *   `feedback_loop_integrator.md`: Implements a feedback loop where the AI presents information and then explicitly asks for user feedback for iterative refinement.
*   **`content_generation/general/`**: Provides general-purpose prompts for creating structured content.
    *   `general_toc_generator.md`: Generates a hierarchical Table of Contents for a book or long document.
    *   `general_chapter_generator.md`: Generates content for a specific chapter based on a ToC item.
    *   `general_content_summarizer.md`: Condenses or summarizes a given piece of text to a specified length or level of detail.
*   **`content_generation/specialized/ai_chan/`**: Contains prompts tailored for a specific AI persona ("AI-chan") focused on educational content.
    *   `ai_chan_course_outline.md`: AI-chan helps create a course outline.
    *   `ai_chan_lesson_generator.md`: AI-chan helps generate lesson content for a course.
*   **`advanced_reasoning/`**: Includes prompts that guide the AI through complex problem-solving using specific reasoning frameworks.
    *   `advanced_cot_problem_solver.md`: Guides the AI to solve problems using Chain-of-Thought (CoT) reasoning, detailing each step.
    *   `advanced_react_problem_solver.md`: Implements a ReAct (Reason-Act-Observe) framework for iterative problem-solving.
*   **`snippets/`**: Contains conceptual building blocks or "snippets" to be inserted into other prompts.
    *   `snippet_persona_loader.md`: A template to define a specific persona for the AI.
    *   `snippet_output_format_specifier.md`: A template to specify the desired output format for the AI's response.

## How to Use These Prompts

1.  **Browse Categories:** Explore the directory structure to find a prompt category and specific prompt relevant to your task or goal.
2.  **Copy and Paste:** The prompts are in Markdown (`.md`) format. Open the file and copy the entire content.
3.  **Input to AI:** Paste the copied prompt directly into your interface with an AI model.
4.  **Replace Placeholders:** Most prompts contain placeholders (e.g., `[Your Name]`, `[User states their problem here]`, `[Persona Name]`, `[Specify the primary format, e.g., Markdown, JSON, XML-like tags, Plain Text, CSV, a specific custom format. Be as precise as possible. For example, for JSON, specify if it's a single object or an array of objects.]`). You **must** replace these with your specific information, context, or requirements to tailor the prompt for your needs.

### Using Snippets

The files located in the `snippets/` directory are conceptual building blocks rather than standalone prompts.

*   **Purpose:** These snippets are designed to be inserted at the beginning of, or within, other prompts (either from this library or your own custom prompts).
*   **Functionality:**
    *   `snippet_persona_loader.md` allows you to define a consistent persona (e.g., "Socratic Tutor," "Technical Expert") for the AI to adopt during the interaction.
    *   `snippet_output_format_specifier.md` enables you to instruct the AI on the precise structure and formatting of its response (e.g., JSON, specific Markdown structure, numbered lists).
*   **Customization:** Combine these snippets with task-specific prompts to highly customize the AI's behavior and output, ensuring it aligns with your expectations for both personality and presentation. For example, you could use the `snippet_persona_loader.md` at the start of the `general_chapter_generator.md` to have the chapter written in a specific style.

By utilizing these prompts and snippets effectively, you can guide AI models to produce more accurate, relevant, and well-structured responses.

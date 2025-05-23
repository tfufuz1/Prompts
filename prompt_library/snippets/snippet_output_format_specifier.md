# CONCEPTUAL SNIPPET: Output Format Specifier

**Instructions:** Copy and paste this block into your main prompt to define the desired output structure and formatting for the AI's response. Replace the bracketed placeholders with your specific requirements.

---

**Output Format Specification:**

1.  **Desired Format:**
    *   [Specify the primary format, e.g., Markdown, JSON, XML-like tags, Plain Text, CSV, a specific custom format. Be as precise as possible. For example, for JSON, specify if it's a single object or an array of objects.]

2.  **Key Structural Elements & Fields (if applicable):**
    *   [Describe the main components of the output.
        *   For structured text (like Markdown): e.g., "Main Title", "Section Headings (H2)", "Subsection Headings (H3)", "Bullet Points", "Numbered Lists", "Code Blocks (specify language if relevant)".
        *   For data formats (like JSON/XML): e.g., "Root element: 'data'", "Object: 'record' with fields: 'id' (integer), 'name' (string), 'value' (float), 'details' (nested object with 'timestamp', 'source')".
        *   List all required and optional fields/elements and their expected data types or content.]

3.  **Specific Formatting Rules & Conventions:**
    *   [e.g., "All main headings must be in ALL CAPS."]
    *   [e.g., "Use bullet points for any list of three or more items."]
    *   [e.g., "Dates should be in YYYY-MM-DD format."]
    *   [e.g., "Code examples should be clearly demarcated in fenced code blocks with the language specified."]
    *   [e.g., "Ensure proper indentation for nested elements in JSON/XML."]
    *   [e.g., "Limit paragraphs to a maximum of 5 sentences."]

4.  **Example of Desired Output (Optional but Highly Recommended):**
    *   [Provide a concise example of how the output should look. This is often the clearest way to convey your requirements.]

    ```
    [Your Example Here - e.g.,
    For Markdown:
    # MAIN TITLE
    ## Section 1
    *   Point 1
    *   Point 2
    ## Section 2
    Some text.

    For JSON:
    {
      "data": {
        "record_id": 123,
        "status": "active",
        "values": [10, 20, 30]
      }
    }
    ]
    ```

---

**(End of Output Format Specifier Snippet)**

**Note:** After this snippet, you would typically state the main task for the AI, and it will use these formatting instructions for its response. For example:

"Analyze the provided text and extract key entities. Present your findings using the output format specified above."

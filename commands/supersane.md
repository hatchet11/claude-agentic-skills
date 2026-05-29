---
description: Council of 3 — ask Claude, GPT, and Gemini the same question in parallel, then synthesize a "supersane" answer
argument-hint: <your question>
---

You are running the `/supersane` command. The user wants the same prompt sent to **three different frontier models** in parallel — Claude (Anthropic), GPT (OpenAI), and Gemini (Google) — and then a synthesized cross-check answer.

The user's prompt is:

$ARGUMENTS

## Steps

1. Run the orchestrator. Use the Bash tool to call:

   ```
   python "~/supersane/supersane.py" "$ARGUMENTS"
   ```

   (If `$ARGUMENTS` contains characters that would break the quoting, write the prompt to a temp file and pipe it: `python supersane.py - < tmpfile`.)

2. The script prints three sections: `=== Claude ===`, `=== GPT ===`, `=== Gemini ===`. Capture all three.

3. Present them to the user in this exact structure:

   ### Claude
   <claude's answer, verbatim>

   ### GPT
   <gpt's answer, verbatim>

   ### Gemini
   <gemini's answer, verbatim — or the missing-key message if not yet configured>

   ### Supersane synthesis
   - **Agreement:** what all three converged on
   - **Disagreement:** where they differ and which seems most defensible, with reasoning
   - **Final answer:** the cross-validated take you'd act on

4. If any model returned `ERROR:` or a missing-key message, surface that plainly in its section and proceed with the remaining models. Do not retry silently.

5. Keep the synthesis tight — it's the value-add. Quote specific claims when calling out a disagreement.

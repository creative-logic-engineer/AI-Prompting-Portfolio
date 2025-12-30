Case Study: Narrative Constraint Engineering
Project Title: High-Fidelity Persona & Style Enforcement

Role: Prompt Engineer / Narrative Strategist

🎯 The Challenge

Standard AI outputs often suffer from "Generic Voice," where the model defaults to a polite, robotic tone. The goal of this project was to engineer a system that forces an LLM to maintain a complex, paranoid persona while adhering to strict vocabulary and frequency constraints.

🛠️ The Solution (The Prompt Architecture)

I designed a multi-layered prompt using XML segmentation to isolate system logic from user data.

Key Engineering Constraints implemented:

Persona Deep-Diving: Established "Silas," a weary clockmaker.

Negative Constraints: Forbidden keywords ("magic," "police") to force creative metaphor.

Frequency Capping: Restricted the high-impact word "pendulum" to a single instance to ensure narrative punch.

Abstract Reasoning: Required the description of a color (Deep Purple/Twilight) without naming the color itself.


<system_instruction>
  <persona>Silas: An aging, paranoid clockmaker in a magic-illegal city.</persona>
  
  <constraints>
    1. NO-GO WORDS: magic, police, illegal, arrest, spell.
    2. MECHANICAL TERMS: Must use 3+ (e.g., escapement, mainspring, gears).
    3. COLOR RULE: Describe a specific color via metaphor only (no naming).
    4. FREQUENCY: The word "pendulum" must be used EXACTLY once.
  </constraints>

  <style>Short, clipped sentences. Weary and mechanical tone.</style>
</system_instruction>

📊 The Result

User Input: "Write a note to daughter Elara warning her about patrols and a repaired music box."

AI Output: > "Elara— The work is finished. I’ve balanced the escapement to within a thousandth of an inch, and the mainspring carries enough tension to last a lifetime. The casing has been polished to the hue of a bruised twilight sky. Stay clear of the shop. The rhythmic boots of the Inspectors are heavy on the cobbles today, and the pendulum of their favor has swung away from us. They are sniffing for the scent of The Static in every doorway. Keep your gears silent. —S"

🧠 Reflections & Optimization

By applying "Zero-Tolerance" logic (honed from my background in Manual Machining), I was able to verify that the model followed 100% of the constraints. This method is highly applicable for gaming studios requiring consistent lore generation or brands requiring strict adherence to a specific "Voice and Tone" guide.


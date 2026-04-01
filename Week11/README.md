# Lab 11 – Fine-Tuning for Real-World Applications

## Objective
Fine-tune a pre-trained generative model (GPT-2) for real-world applications to build a Product Review Generator for e-commerce and a Recipe Instruction Generator for a food-tech application.

## Workflow

### Component I: Product Review Generator (E-Commerce)
- Load GPT-2 and generate baseline product reviews.
- Prepare and tokenize the e-commerce product review dataset.
- Fine-tune the model on the product review data.
- Generate new product reviews and compare them with the baseline output.

### Component II: Recipe Instruction Generator (Food-Tech)
- Reload a fresh pre-trained GPT-2 model.
- Prepare and tokenize the recipe instruction dataset.
- Fine-tune the model on the recipe data.
- Generate cooking instructions using dish name prompts and compare them with the baseline.

## Expected Output
- **Baseline:** Generates random, generic text (e.g., Wikipedia-style content).
- **Fine-Tuned (E-Commerce):** Generates realistic product reviews with appropriate tone, vocabulary, and structure (e.g., "amazing battery life", "highly recommend").
- **Fine-Tuned (Food-Tech):** Generates step-by-step cooking instructions including ingredients, preparation steps, and timing.

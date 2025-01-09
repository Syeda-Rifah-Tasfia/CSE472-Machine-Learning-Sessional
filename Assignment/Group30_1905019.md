# Review of "Shadowcast: Stealthy Data Poisoning Attacks Against Vision-Language Models" Blog

#### Blog by: Group 10

#### Review written by: Syeda Rifah Tasfia - 1905019 (Group 30)

---
This blog discusses **Shadowcast**, a novel and stealthy data poisoning attack targeting Vision-Language Models (VLMs). Unlike traditional poisoning methods, Shadowcast injects visually indistinguishable poisoned image-text pairs into training data, manipulating model behavior while evading human detection. Two attack types are highlighted:

1. **Label Attack**: Misclassifies identities or classes (e.g., mistaking Donald Trump for Joe Biden).
2. **Persuasion Attack**: Generates false narratives (e.g., portraying junk food as healthy).

The attack leverages the following mechanisms:

- **Text Generation**: Refining captions of poisoned images using a language model to align with the target concept (destination concept $C_d$), ensuring coherence and emphasis on the desired narrative.
- **Image Perturbation**: Creating visually similar but imperceptibly modified images that align with both the original ($C_o$) and destination concepts ($C_d$) in latent feature space.


## Attacker's Capabilities and Knowledge
Shadowcast operates in both **grey-box** and **black-box** scenarios:
- **Grey-box**: Access to the VLM's vision encoder.
- **Black-box**: No direct access; uses an alternative open-source VLM.

The attacker’s capabilities include injecting stealthy poison samples (image/text pairs) into training datasets without controlling the model during or after training. The attack relies on a “clean-label” approach, making poisoned samples harder to detect.


## Impact and Findings

- Shadowcast influences VLMs to generate manipulated responses to benign user prompts.
- It is effective with minimal poisoned samples and resilient to augmentation and compression.
- The attack is applicable across various VLM architectures and real-world conditions.


## Limitations

The blog acknowledges the lack of exploration into defense strategies, highlighting challenges such as compatibility with VLM-specific loss functions, computational demands, and potential performance trade-offs.

## Conclusion
Shadowcast reveals critical vulnerabilities in VLMs, demonstrating the need for robust defense mechanisms to prevent poisoning attacks and ensure the responsible deployment of these models.
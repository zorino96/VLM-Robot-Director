# VLM as a Robot Director: A Hierarchical Framework for Robotic Control

This project is a proof-of-concept demonstrating how a Vision-Language Model (VLM) can act as a high-level "director" for a robot, translating natural language commands into physical actions in a simulated environment.

## Architecture

The system uses a hierarchical, "Director-Actor" architecture:

1.  **The Director (VLM - LLaVA 7B):** This is the high-level brain. It receives a natural language command (e.g., "Wave at the red box") and an image of the current scene. Its task is to understand the command, perceive the scene, and select the appropriate low-level skill to execute.

2.  **The Actor (Skill Library & Executor):** This is the low-level motor control system. It consists of:
    *   A **Skill Library**: A pre-defined set of simple, reliable animations (e.g., `wave_hand`, `point_forward`).
    *   A **Skill Executor**: A function that takes the name of a skill (chosen by the Director) and executes its corresponding animation in the PyBullet simulation.

This approach effectively bridges the gap between abstract language and concrete physical action.

## Results

As demonstrated in the video below, the system can successfully:
-   Perceive a scene with multiple objects.
-   Understand distinct natural language commands.
-   Select the correct skill from the library to fulfill the command.

https://github.com/YOUR_USERNAME/VLM-Robot-Director/assets/YOUR_USER_ID/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx


## How to Run

1.  Open the `VLM_Robot_Director.ipynb` file in Google Colab.
2.  Ensure your Colab runtime is set to a **GPU** (e.g., T4 GPU).
3.  Add your Hugging Face Access Token as a secret named `HF_TOKEN`.
4.  Run all cells in the notebook.

## License

This project is licensed under the MIT License.

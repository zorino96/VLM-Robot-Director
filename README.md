# VLM as a Robot Director: A Hierarchical Framework for Robotic Control

This repository contains the source code and results for our research on a hierarchical control system for robots. This project demonstrates how a Vision-Language Model (VLM) can act as a high-level "director" to translate natural language commands into physical actions in a simulated environment.

The full research paper and dataset are permanently archived on Zenodo with the following DOI: **[DOI will be generated here after publishing on Zenodo]**

## Architecture

The system uses a hierarchical, "Director-Actor" architecture:

1.  **The Director (VLM - LLaVA 7B):** The high-level brain that understands language and vision. It receives a user command (e.g., "Wave at the red box") and an image of the scene, and then selects the appropriate low-level skill.

2.  **The Actor (Skill Library & Executor):** The low-level motor control system. It contains a pre-defined set of reliable animations (skills) and executes the one chosen by the Director in the PyBullet simulation.

This architecture effectively bridges the gap between abstract language and concrete physical action.

## Demonstration

The final experiment demonstrates the VLM successfully directing the robot to perform two different tasks based on natural language commands.

**Click the image below to watch the full video demonstration on Google Drive:**

[![Robot Director Demonstration](https://drive.google.com/file/d/1kMxuQHScxOuj786LnRaiRNj-wUNOyoIw/view?usp=sharing)]

(https://drive.google.com/file/d/1P5UezIHvvl2zxNY1kDf-CMzrnnP-Zger/view?usp=drive_link)

*In the video, the VLM is tasked with: 1) "Wave at the red box," and 2) "Point towards the blue sphere." It correctly selects the appropriate skill for each command.*

## How to Run

1.  Open the `VLM_Robot_Director.ipynb` notebook in Google Colab.
2.  Ensure your Colab runtime is set to a **GPU** (e.g., T4 GPU).
3.  Add your Hugging Face Access Token as a Colab secret with the name `HF_TOKEN`.
4.  Run all cells in the notebook to reproduce the experiment.

## Cite This Work

If you use this code or research in your work, please cite it using the DOI provided at the top of this README.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

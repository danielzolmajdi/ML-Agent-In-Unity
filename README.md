# ML-Agent-In-Unity

## Overview

This project demonstrates the integration and use of Machine Learning Agents (ML-Agents) in Unity to create intelligent, interactive agents for games and simulations. Unity ML-Agents is an open-source toolkit that enables games and simulations to serve as environments for training machine learning algorithms.

## Features

- **Unity Environment Setup**: Example Unity scene with agents ready for training.
- **ML-Agent Integration**: Uses the official Unity ML-Agents Toolkit.
- **Custom Reward Functions**: Easily modify and experiment with reward shaping.
- **Training Scripts**: Sample Python scripts and configuration files for training agents.
- **Pre-trained Models**: Include and use pre-trained models for inference.
- **Documentation and Tutorials**: Step-by-step guidance to get started and experiment.

## Getting Started

### Prerequisites

- [Unity](https://unity.com/) (Recommended: LTS version, e.g., 2021.3+)
- [Unity ML-Agents Toolkit](https://github.com/Unity-Technologies/ml-agents)
- Python 3.6+ (for training)
- `mlagents` Python package

### Installation

1. **Clone this repository:**

   ```bash
   git clone https://github.com/danielzolmajdi/ML-Agent-In-Unity.git
   ```

2. **Open the project in Unity:**
   - Launch Unity Hub.
   - Click "Add" and select the project folder.

3. **Install ML-Agents Toolkit:**
   - In your terminal, create and activate a virtual environment:
     ```bash
     python -m venv venv
     source venv/bin/activate  # On Windows: venv\Scripts\activate
     ```
   - Install ML-Agents:
     ```bash
     pip install mlagents
     ```

### Training an Agent

1. **Configure the Agent:**
   - Open Unity, select the sample scene with the agent.
   - Ensure the agent uses the correct Behavior Parameters.

2. **Start Training:**
   - In the Unity Editor, go to `Edit > Project Settings > Player` and enable the necessary API compatibility.
   - In your terminal, run:
     ```bash
     mlagents-learn config/trainer_config.yaml --run-id=MyFirstRun
     ```
   - Press Play in the Unity Editor to begin training.

3. **Observing Training:**
   - Training metrics will appear in the terminal and TensorBoard.

### Using a Trained Model

- Once training is complete, place the trained `.onnx` model file into the appropriate Unity Assets folder.
- Assign the model to your agent's Behavior Parameters.

## Project Structure

```
ML-Agent-In-Unity/
├── Assets/
│   ├── Scenes/
│   ├── Scripts/
│   └── Models/
├── config/
│   └── trainer_config.yaml
├── README.md
└── ...
```

## Resources

- [Unity ML-Agents Toolkit Documentation](https://github.com/Unity-Technologies/ml-agents/blob/main/docs/Readme.md)
- [ML-Agents GitHub Repository](https://github.com/Unity-Technologies/ml-agents)
- [Unity Documentation](https://docs.unity3d.com/)

## Contributing

Contributions are welcome! Please open issues or pull requests for improvements, new environments, or bug fixes.

## License

This project is licensed under the MIT License.

---

**Created by [danielzolmajdi](https://github.com/danielzolmajdi)**

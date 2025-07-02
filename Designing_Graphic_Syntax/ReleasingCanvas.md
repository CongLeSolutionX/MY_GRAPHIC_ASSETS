

<details open>
<summary>Click to show/hide the full disclaimer.</summary>
   
> <ins>📢 **Disclaimer** 🚨</ins>
>
> This is a sketch book where I actively experiment and try new techniques<br/>
> and get result in realtime for faster development.</br>
> It's where I document my academic explorations,</br>
> share my findings with anyone interested,</br>
> and maintain a personal vault of my creative and technical journey.</br>
> I'm not sure the link for this repo being shared in the back by others,</br>
> since I havent plan for any analytics for this project yet.</br>
> ...and I'm actively looking for a job...</br>

> This document contains my personal notes on the topic,</br>
> compiled from publicly available documentation and various cited sources.
> 
> The materials are intended for educational purposes (<ins>sometimes, entertainment purposes</ins>), personal study, and technical reference.
> The content is dual-licensed:
> 1. **MIT License:** Applies to all code implementations (Swift, Mermaid, and other programming languages).
> 2. **Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0):** Applies to all non-code content, including text, explanations, diagrams, and illustrations.

</details>



---




~~~mermaid
---
title: "High-Level System Overview"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY 4.0"
copyright: "Copyright (c) 2025 Cong Le. All Rights Reserved."
config:
  layout: elk
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%%%%%%% Available curve styles include the following keywords:
%% basis, bumpX, bumpY, cardinal, catmullRom, linear, monotoneX, monotoneY, natural, step, stepAfter, stepBefore.
%%{
  init: {
    'flowchart': { 'htmlLabels': true, 'curve': 'basis' },
    'fontFamily': 'Monaco',
    'themeVariables': {
      'primaryColor': '#D521E3',
      'primaryTextColor': '#F8B229',
      'lineColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#2DF2',
      'secondaryTextColor': '#6C3483',
      'secondaryBorderColor': '#A569BD',
      'fontSize': '15px'
    }
  }
}%%
flowchart LR
    User@{ img: "https://github.com/CongLeSolutionX/MY_GRAPHIC_ASSETS/blob/Designing_graphic_syntax/MY_MEME_ICONS/Orange-Cloud-Search-Icon-Base-Color-Black-1024x1024.png?raw=true", label: "User", pos: "b", w: 100, h: 100, constraint: "on" }

    User -- Speaks Vietnamese --> SpeechRecognizer
    SpeechRecognizer -- Transcribes --> AICardView(("AICardView"))
    AICardView -- Contains --> UserInterface
    AICardView -- Handles Input --> RecordingController
    AICardView -- Handles Output --> PlaybackController
    AICardView -- Triggers --> AIInteraction
    AIInteraction -- Calls --> LLMModel(LLM Framework)
    LLMModel -- Processes Question --> AIResponse
    AIResponse -- Returns to --> AIInteraction
    AIInteraction -- Updates --> AICardView
    AICardView -- Displays --> AIResponse
    AICardView -- Sends to --> TextToSpeech
    TextToSpeech -- Speaks Vietnamese --> User

    subgraph Voice_Input["Voice Input"]
    style Voice_Input fill:#22f,stroke:#333,stroke-width:1px
        direction LR
        SpeechRecognizer
        RecordingController
    end

    subgraph Voice_Output["Voice Output"]
    style Voice_Output fill:#c1d2,stroke:#333,stroke-width:1px
        direction LR
        TextToSpeech
        PlaybackController
    end

    style LLMModel fill:#212,stroke:#333,stroke-width:2px
    style AICardView fill:#c229,stroke:#333,stroke-width:2px

~~~



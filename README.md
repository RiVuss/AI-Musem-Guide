# 🎨 Interactive Museum Guide MVP

This repo has the code for an MVP for an **Interactive Museum Guide**, designed to enhance visitor engagement through **Facebook Messenger**. I built this project in 2023 during my entrepreneurship minor.

The museum visitors could ask a digital tour guide questions about the exhibits or their artists, satisfying their curiosity.

---

## ✨ Features

- **AI-powered Conversations**: Utilized **Llama-2-7b-chat** running locally to simulate interactive dialogue.
- **Real-time Interactions**: Visitors could ask questions or request information about exhibits via **Facebook Messenger**.
- **Practical Showcase**: Tested with museum visitors, demonstrated at the **UvA Entrepreneurship Minor Startup Market**, and presented to museums as a technological prototype.

---

## 🔧 Methodology & Technologies

- **Large Language Model (LLM)**: Deployed **Llama-2-7b-chat** locally to process and generate natural language responses.
- **Backend Framework**: Built using **Flask** for handling API requests and interaction logic.
- **Messenger API Integration**: Connected the bot to **Facebook Messenger** for real-time user interaction.
- **Tunneling for Local Testing**: Employed **ngrok** to expose the local server to the web, facilitating interaction through Messenger.
- **Testing & Feedback**: Conducted initial user testing with museum visitors to gather insights into usability and performance.

---

## 📚 Libraries Used

The project uses the following libraries to implement its features:

- **torch**: For running the Llama-2-7b-chat model locally.
- **transformers**: For interfacing with the pre-trained Llama-2-7b-chat model.
- **flask**: For creating the backend server and handling API requests.
- **pymessenger**: For connecting the bot with the **Facebook Messenger API** and handling interactions.
- **BitsAndBytes**: Used within **transformers** for model quantization, enabling efficient usage of LLMs on consumer-grade hardware.
- **requests**: To manage HTTP requests for integration and external API communication.

---

## 🚧 Challenges & Learnings

- **Quantization Limitation**: The **BitsAndBytes** library (within transformers) used for model quantization did not support Windows, requiring running the code on **Linux**.
- **Museum Planning Horizons**: The project faced adoption hurdles due to the long planning cycles of museums, preventing integration into live exhibitions.
- **User Feedback**: Users really enjoyed the interactive nature of the guide; however, concerns about the **factuality of the responses** remained, highlighting a common limitation with LLMs. It would be interesting to experiment with newer, larger models with extended context windows to provide more comprehensive information to the LLM about the artwork, which could potentially address these concerns.

---

## 🌍 Legacy: KurioCity

The foundational ideas of this project evolved into **KurioCity**, a web app offering **AI-generated audio guides** for landmarks across Amsterdam, creating a city-wide museum experience. You can check out the project website at [kuriocity.com](https://kuriocity.com).

---

## 📂 Repository Content

- **Notebook**: `MessengerBotGeneralQueryNoToken.ipynb` - This notebook contains an instance of the bot with a general 3-shot prompt, designed to answer questions about any artwork.
- **Notebook**: `MessengerBotSpecificPrompts.ipynb` - This file contains an instance of the bot with multiple preloaded prompts, each tailored to a specific museum exhibit. The approach aimed to provide the LLM with exhibit-specific information to limit hallucinations and enhance response accuracy. The prompt was selected by starting the user message with a number to identify the exhibit, similar to other museum audio guides.

---

## 💬 Example Interactions

Here are some sample interactions that demonstrate the capabilities of the interactive museum guide:

1. **User Question**: *Are there any notable figures in it?*

   **Response**: *Yes, indeed! Look closely at the left bank; you'll spot several important figures, including Prince Maurice of Orange, Prince Frederick Hendrik, King James I of England, King Christian IV of Denmark, and a young King Louis XIII of France accompanied by his mother, Queen Marie de' Medici. And on the right bank, you'll recognize Governor Albert and Isabella, Commander-in-Chief Ambrosio Spinola, and Pope Paul V being carried in a sedan chair by his cardinals. Van de Venne included these personalities to emphasize the religious and political divisions present throughout the country during that era.*

2. **User Question**: *Why did PC Hooft have multiple paintings made by Mierevelt?*

   **Response**: *According to historical records, Michiel van Mierevelt painted at least three portraits of P.C. Hooft during his lifetime. These portraits provide valuable insights into Hooft's personal style, mannerisms, and attire, reflecting the changing fashions of the era. Each portrait offers a unique perspective on Hooft's character and personality, demonstrating the artist's skill in capturing subtle details and nuances. This diversity of images has contributed significantly to our understanding of both Hooft and Van Mierevelt's oeuvre.*

3. **User Question**: *How does this painting relate to Attack On Titan?*

   **Response**: *Thank you for asking! While "The Fishing for Souls" doesn't directly relate to Attack on Titan, both works deal with themes of struggle and survival. Both paintings feature groups of people fighting against adversity, whether it be the religious and political conflicts in the Netherlands or the titans threatening humanity in Attack on Titan. Additionally, both works explore ideas of faith, perseverance, and the importance of community in overcoming challenges. So while they may seem unrelated initially, there are actually some interesting connections to be made between these two works of art.*

---

## 🙏 Acknowledgments

I would like to thank all the people who interacted with me during the **UvA Entrepreneurship Minor Startup Market**, as well as all the museum visitors who agreed to talk to me and try out this prototype. Your insights and feedback were invaluable to this project's development.

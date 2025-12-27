## UC Berkeley AI Hackathon 2024
Mithil
Charlotte
Juli
Medhavi


## What it does
911-rEsQ revolutionizes emergency response by leveraging advanced AI technology to optimize communication between callers and 911 operators. This groundbreaking application processes audio from 911 calls, effectively cleaning up background noise and enhancing the clarity of the caller's message. By improving language comprehension, 911 operators can swiftly understand critical details even in chaotic environments.

Moreover, 911-rEsQ goes beyond mere audio enhancement. It scans for crucial background sounds such as faint gunshots or distressed screams, providing operators with vital situational context to assess the severity of emergencies accurately. This capability enables operators to make informed decisions on dispatching appropriate resources, whether police, medics, or other responders, swiftly and accurately.

In addition to its audio processing capabilities, the application analyzes the caller's emotional state. By detecting tones of distress or urgency, 911-rEsQ helps operators manage and prioritize calls effectively. This feature not only assists in distinguishing genuine emergencies from accidental or prank calls but also supports operators in calming panicked callers and gathering crucial information efficiently.

By equipping 911 operators with enhanced audio clarity, real-time danger signal detection, and emotional analysis tools, 911-rEsQ significantly enhances emergency response capabilities. This innovation ensures that every call receives the urgent attention it deserves, potentially saving lives in critical situations where every second counts.

## How we built it
The project employs Python libraries such as sounddevice, AudioSegment from pydub, scipy, librosa, and noisereduce to enhance the clarity of audio from 911 calls. These libraries are crucial in to clean up background noice and improving sound quality and the comprehensibility of caller voices, ensuring that 911 operators can effectively understand crucial details even in noisy environments where every second counts.

Moreover, the project utilizes Hume AI's Expression Measurement API and websockets for analyzing the emotional states of callers based on their voice tones and patterns. This emotional analysis component provides operators with insights into the urgency and severity of each call, enabling them to prioritize responses accordingly. This will output the top 5 emotions detected by Hume AI's API to give operators more insight on the urgency and authenticity of the call. Simultaneously, a PyTorch-based model is developed to detect critical background noises, such as gunshots or screams in the audio. This capability enhances situational awareness for operators, allowing them to swiftly dispatch appropriate emergency resources.

To integrate all these functionalities into a unified application, the project utilizes Flask and Streamlit for backend development and HTML/CSS for frontend interface design. Flask and Streamlit manages the backend processes, including audio enhancement, emotion analysis, and noise detection. This integration ensures seamless communication and real-time information display, enabling operators to make informed decisions promptly during emergencies.

As part of our project, we retrained the Microsoft’s Contrastive Language-Audio Pre Training model, which offers zero-shot classifications, so we tailored it towards detecting not only gunshots and screams but fires, footsteps, breathing patterns, and other life-threatening sounds as well. However, this feature is not yet integrated into our Streamlit app. Before integration, we need to isolate background audio to ensure accurate classification, as the presence of talking can dominate the audio stream and affect the classification results. This additional step will enhance the effectiveness of our application in detecting and responding to critical emergencies.

## Challenges we ran into
Integrating HumeAI for audio analysis initially presented challenges due to its specific application in our project. We had to explore and understand how to effectively utilize Hume AI's capabilities to analyze the intricate details of audio data from emergency calls. In the end, we decided to go with their Expression Measurement API as it is a perfect fit for the purposes of our project. This process involved tackling technical obstacles such as data preprocessing, ensuring seamless integration of the model into our system, and deciphering the output to derive meaningful insights into caller emotions and the context of each emergency situation.

Similarly, we faced various challenges while developing the PyTorch CNN. As beginners in AI and machine learning, we faced a steep learning curve in understanding and utilizing the PyTorch framework. The task of building and refining the classification model required deep dives into fundamental concepts such as neural network architecture, optimization techniques, and effective training methodologies. Some challenges we faced included setting up the development environment, debugging code to achieve desired functionalities, and rigorously validating the model's accuracy and ability to perform in realistic emergency scenarios.

## Accomplishments that we're proud of
We are incredibly proud of our team as this Hackathon experience demonstrated our ability to collaborate effectively and use our technical skills to address pressing timely societal and safety issues. As students in the United States, where school shootings are unfortunately common, this project was particularly meaningful to us. We were proud to develop a solution that has the potential to save lives, aid victims, and improve emergency response. Throughout the process, we pushed ourselves to learn new technologies over the weekend and created working models that can positively impact the lives of many people.

We hope to continue fueling the fight to address the unfortunate reality that school shootings remain a significant issue in our society. We are also very proud that our project is applicable in numerous situations not only school shootings, but abduction victim calls, domestic violence situations, and more. Moreover, our project highlights the transformative power of technological advancement in addressing critical societal challenges and social impact. This project was more than just a hackathon; it was a stepping stone towards our aspirations to drive positive change in our communities!

## What we learned
We found it deeply rewarding to apply AI technologies and methods to assist 911 operators in responding to calls from victims. Given the ongoing issue of school shootings in society, we take pride in raising awareness through an innovative solution that aids 911 operators and improves the chances of protecting victims. We are thrilled to have utilized our software expertise to create something that will positively impact many lives.

Our primary focus this weekend was on developing models to classify faint audio. We gained proficiency in processing and refining audio, analyzing faint sounds for specific characteristics. Additionally, we acquired skills in using ML frameworks like PyTorch and exploring AI applications such as HumeAI, all while advancing our capabilities in web development and data analysis.

## What's next for 911 rEsQ
The next step for 911 rEsQ involves advancing the integration of real-time audio capabilities into our project. Currently, we have achieved basic functionalities such as audio recording and real-time enhancement using our application. Our immediate objective is to seamlessly integrate these capabilities into HumeAI, enhancing the overall efficiency and effectiveness of emergency response operations.

Furthermore, our plan includes collaborating with local governments to implement our application within their call centers. By doing so, we aim to empower emergency responders with advanced tools that can significantly improve their response times and outcomes during critical situations, such as school shootings and other emergencies. This initiative reflects our commitment to leveraging technology to enhance public safety and support the vital work of emergency services nationwide.


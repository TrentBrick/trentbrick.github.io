---
layout: post
title: My PhD Thesis
date: 2025-03-31 11:29:0 +0000
comments: True
categories: [Publications]
---

*My thesis is on the Interwebs!*

---

My thesis is now live on the interwebs! I'm [hosting it on my website here](../documents/PhDThesis-Sparse_Representations_in_Artificial_and_Biological_Neural_Networks.pdf) but honestly it's just four of my papers stapled together which you can read elsewhere. The only new content is the introduction which I tried pretty hard to make an accessible overview. I'm quite pleased with it so here it is reproduced below. I will also reproduce the Acknowledgements section and Dedication :)

---

## Introduction

Human intelligence is a key reason you are currently reading this thesis instead of running away from a lion on the African Savannah. Our extraordinary brains have elevated humanity from a precarious existence as hunter-gatherers to the dominant species capable of reshaping the planet.

Yet for all its power, human intelligence remains mysterious. We understand the broad strokes: our brains contain billions of neurons connected by trillions of synapses, forming networks that somehow give rise to cognition. But beyond this general framework, the specifics of intelligence remain elusive. We don't fully understand how memories form, how concepts are represented, or how reasoning unfolds at a mechanistic level. Moreover, it is unclear what level of abstraction, from individual neurons to broader circuits and systems, is key for understanding intelligence. The brain is arguably the most complex system we've ever attempted to reverse engineer, and we're still in the early stages of that journey.

Artificial Intelligence (AI) presents a similar puzzle. Despite being capable of remarkable feats - from defeating the world's best Go players to generating text indistinguishable from human writing - we don't have a comprehensive understanding of how AI works. Even with full access to the AI's architecture, weights, and activations, tracing the path from input to output in a way that meaningfully explains the system's reasoning remains challenging. This is because, while we have created it, state-of-the-art AIs are "grown", not built.

Uncertainty on both fronts contributes to ongoing debates about whether artificial neural networks and biological brains employ fundamentally similar or different mechanisms. Some researchers argue that, just as birds and planes work in very different ways, so too do minds and machines. The argument goes that silicon hardware is very different from neuronal wetware and the evolutionary process that created our brains will look nothing like that which creates AI. Put another way, we are "teaching sand to think" and there is no reason it should think like us.

While these arguments are compelling, this thesis explores the other side of the debate, investigating where today's artificial intelligence already has, or would benefit from, convergence with algorithms used by the brain. Although birds and airplanes may not fly exactly the same way, when you look beyond their raw materials, they have a lot in common: both share similar aerodynamic profiles, use wings and control surfaces like tail rudders, and leverage the same flight mechanics of lift, thrust, and drag.

Similarly, any intelligence will need to perform the same core informational processing such as extracting meaningful signal from vast quantities of noisy input data; remembering the information that will be useful; storing it in a way that it can be easily retrieved when relevant; and using it to best achieve future goals.

Beyond sharing core informational processes, AI is being trained to perform human tasks and is powered by ideas from our own biology and psychology. One of the recent breakthrough algorithms in AI, that this thesis connects to a key circuit in biological brains, is literally called "Attention". "Attention" was inspired by the human ability to pay attention to a small number of things while ignoring distractions, for example, by focusing on a conversation inside a busy restaurant.

Finally, as much as we researchers pride ourselves on the ability to theorize and plan ahead, AI research follows the scientific tradition of trial-and-error breaking the trail of discovery, with theoretical understanding playing catch-up. This makes our search for the recipe behind intelligence look more like the process of evolution than we researchers may otherwise care to admit.

Regardless of philosophically exploring the reasons \textit{why} artificial intelligence may to converge on a similar design to the human brain, this thesis presents four examples of such convergence occurring.

Taken together, these chapters have a unifying theme around sparse representations. "Sparsity", defined as "something thinly dispersed or scattered", refers here to sparse neuron activity, where only a small fraction of the total number of neurons are active at any time. "Representations", refers to how data is encoded. For example, using only 10 neurons out of 10,000 in your brain to encode an image of a lion would be an example of a sparse representation.

We begin in Chapter 1 by showing how a theoretical model of human memory is not only the most common circuit in the brain but also a close approximation to the breakthrough "Attention" algorithm powering state-of-the-art AI models. This memory model, Sparse Distributed Memory (SDM) has a compelling biological mapping to the cerebellum, a brain region which contains $\sim$80\% of our neurons and exists in most organisms including fruit flies  (Essen et al., 2018). We show in particular that the way SDM chooses to write and read memories closely approximates the approach taken by Attention, suggesting that these seemingly distinct approaches converge on similar computational principles. This link provides a fresh perspective on why the Attention mechanism works so effectively in modern AI systems while simultaneously offering a computational interpretation of cerebellar function.

Chapter 2 shows that we can use additional structures from our own cerebellum to solve memory problems with artificial networks. Many AI models will forget existing knowledge when they are taught something new because they overwrite the previous information. Sparse Distributed Memory, by introducing sparsity, allows the AI to develop on its own specific memory modules that are overwritten less often. These modifications are inspired by inhibitory interneurons in the cerebellum not accounted for in the original SDM model. By systematically testing the contribution of each biologically-inspired component, we show that this approach offers a compelling alternative to existing continual learning techniques, which often rely on hand labelling different types of information.

Chapter 3 shows how simulating a more human-like learning environment with noisy inputs causes artificial neural networks to look more brain-like. Specifically, adding random noise to training data causes artificial neural networks to become sparse. The presence of noise and resulting sparsity cause the artificial network to more closely resemble a biological brain. Furthermore, when trained on image data, the network spontaneously develops receptive fields that look a lot like those found in biological visual systems. We mathematically derive three implicit loss terms introduced by this noisy training to explain these emergent properties.

Chapter 4 uses ideas about how the human brain encodes and decodes information to make AI models more transparent. There is a major open challenge to reverse-engineer the brains of AI language models like ChatGPT and Claude. Why did the model refuse a completely harmless request? Is it telling users only what they want to hear or what it actually believes? Can the AI be trusted? These important questions are difficult to answer because these AI models represent concepts using incredibly dense, intertwined representations. Any component of the model is involved in a hundred different behaviors and cannot be isolated to work out what part it is playing. We call this dense intertwining of representations "superposition" and an analogy is a photograph that has been exposed multiple times: imagine placing multiple transparent sheets on top of each other, each one printed with a different pattern or image. As you stack more layers, the original images visually blend together, making it harder to focus on any individual component. The stack of transparencies ends up holding compressed information from all the original images superimposed together.

To tackle this problem, we introduce "sparse autoencoders" as a method for "undoing" this superposition, pulling apart each of the transparent sheets so they separately display their own image. The end result is a collection of tens of thousands of neatly separated "features", each corresponding to a meaningful concept that the network has learned. This technique is providing novel insights into how AI models organize information and is a stepping stone towards making them more transparent and controllable. There are two connections to biological brains with this work. First, the way we decode superposition builds directly on work around sparse coding from reseach around how the brain represents images. Second, the conditions that make superposition a powerful compression strategy for AI models are likely to also exist in the brain and have been discussed for a long time under the term "population coding". As a result, it is likely that our decoding technique will also work for brain data with new collaborations underway.

The study of sparse representations in neural networks has a rich history spanning neuroscience, machine learning, and theoretical computer science. In the brain, sparsity of neural activity has been a well-observed phenomenon (Purves et al., 2001) and has been proposed as a fundamental principle underlying sensory processing, particularly in the visual cortex  (Olshausen and Field, 1997, 2004).
In artificial neural networks, sparsity has been explored through various approaches including sparse coding and its approximations like sparse autoencoders (Olshausen and Field, 1997a; Makhzani and Frey, 2014a). These methods aim to learn compact, interpretable representations that can improve computational efficiency, generalization, and robustness (Ahmad and Scheinkman, 2019; Kurtz et al., 2020; Yang et al., 2020; Aljundi et al., 2019b; Abbasi et al., 2022; Smith et al., 2022). Insights from neuroscience have inspired several advances in artificial intelligence. For example, the development of convolutional neural networks drew inspiration from the hierarchical organization of the visual cortex (LeCun et al., 1989; Krizhevsky, 2009), meanwhile Dropout was inspired by the stochasticity of neural activity (Srivastava et al., 2014).

The bidirectional flow of ideas - from biology to AI and back again - can enrich our understanding of both. Computational models inspired by biology can be tested and refined in ways that would be impractical in biological systems, potentially generating new hypotheses about neural function. Conversely, the surprising emergent properties of artificial systems can suggest new ways of thinking about biological processes.

In the chapters that follow, we will explore this interplay between biological inspiration and artificial implementation, with a particular focus on how sparse representations emerge, function, and can be manipulated in neural systems. Through this exploration, we hope to contribute to our understanding of intelligence in both its natural and artificial forms, and to advance the development of AI systems that can learn continuously, represent information transparently, and ultimately serve human needs more effectively.

---

## Acknowledgements

There are too many people to thank and acknowledge. It really takes a village. There is that saying "you are the average of the five people you spend the most time with," but I don't think, at least in my case, it should stop at five. It is too easy for me to trace the source of any accomplishments back to the influence of others. I truly have continued to be in the right place at the right time.

Thanks first to Maxwell Kanter, Kayla Colvin, Jason Wang, Brett Mathias, Rowly Graham and Joshua Rollins for reading and sharing feedback on the introduction to this thesis. If it is at all readable, it is thanks to you.

Thanks to Joe Choo-Choy, Miles Turpin, and Max Farrens, you are the most fantastic friends anyone could hope for. Your integrity, thoughtfulness, and kindness have made me a better person. Your curiosity and encouragement have kept me doing research and having fun with it. Joe, I am so lucky to have been in the same boarding house with you for high school and then share another three years at the same university. It takes two to make a tribe and you were my tribe in high school, enabling me to be a weirdo and pursue idiosyncratic interests. Reading Nick Bostrom's Superintelligence with you senior year was particularly formative and first sparked my interest in neuroscience, AI, and the foundations of intelligence. Miles, you immediately joined the tribe in undergrad and have been part of it ever since. You made it cool to wear ten dollar dark orange construction glasses that block blue light before bed and first explained gradient descent to me during a Sunday morning breakfast the first semester of our freshman year. Max, your influences started far earlier when we were five. A motivation for me has always been wanting you to think I'm cool. Your enthusiasm for every one of my pursuits is highly contagious, whether it was making bad artwork for one of your albums or designing a financially ruinous crypto art NFT. Joe, Miles, and Max, have all been there for me during the highest highs and the lowest lows. Thank you for making life so meaningful.

Thanks to Nathan Rollins for being an incredible academic mentor in addition to a friend. Your supervision when I was a bright-eyed intern in Dr. Debora Marks's lab at Harvard Medical School taught me how exciting science can be. Your meteoric career trajectory has made me more ambitious. Your advice on my PhD applications is the reason I had my choice of graduate schools and was able to find the best fit to thrive.

To Dr. Debora Marks, answering my cold email to intern in your lab my Junior summer was the launchpad for my scientific career. Until that point I was starting to believe that science was for stale, esoteric, boring questions. By the end of that summer, you had given me the opportunity to work: on a DARPA project to modify extremophile proteins to work in humans; an IARPA project to rapidly identify immune system evasion genes in viruses, and a side hustle to grow giant insects! I hope I have learned some fraction of your ability to pursue ambitious research and always ask the right questions.

To Dr. Robert Thompson, who enabled me to first cultivate an interest, and ultimately create my own undergraduate major, in "Biological and Artificial Intelligence". You let a random Sophomore meet with you weekly to discuss papers on human intelligence, brain development, and nutrition as one of my four semesterly courses. Having the time and support to pursue this reasearch was pivotal to me creating my major which you then sponsored and supervised for the remainder of my undergraduate degree. Thank you for giving me the nutrients to grow.

To Dr. David Banks, for teaching me statistics and deep learning. Agreeing to an independent study where we read Ian Goodfellow et al.'s Deep Learning textbook was prescient. I feel lucky to have witnessed your humility, intelligence, and curiosity to learning all there is about the world over many coffee chats across many years. Thank you for continuing to arrange such conversations remotely and remain in touch.

To Julian Robertson, whose scholarship program in undergrad gave me the funding and tokens of prestige I would have otherwise wasted time seeking. This enabled me to instead pursue research and be funded at Harvard Medical School with Dr. Debora Marks. I likely would not have known about, or been qualified for my PhD research, without this experience.

To Dr. Andrew Murray. At the very start of our PhD program, you said, "I don't care what you do, as long as you do the best beeping research you can." And I knew that this was the program for me. I hope it is okay that I took your advice so literally -- I know this PhD has been unconventional -- but I believe I have been able to do the best research I can and might not have without your vision.

To Dr. Cengiz Pehlevan, for getting me to dream big and execute on those dreams. I never thought my first paper, which started as a final project in your class  my very first semester of graduate school, would ever become a paper at NeurIPS.

To Dr. Bruno Olshausen and Pentti Kanerva, for being such wise and enthusiastic collaborators. You both made it possible for me to be a visiting researcher at Berkeley's Redwood Theoretical Neuroscience Institute which was a highlight of my PhD. It has been an honor to take your research and build upon it in minor ways.

To my committee, Dr. Demba Ba, Dr. Sam Gershman, and Dr. Sean Eddy, I greatly admire your research and it is a privlege to have you evaluate me as a PhD candidate. Your guidance across multiple pre-qualifying exams and other check-ins has made my work more relevant and rigorous.

To Dr. Gabriel Kreiman, without whom this PhD never would have happened -- many times over! Publishing "Attention Approximates Sparse Distributed Memory" unlocked multiple exciting research avenues that I wanted to chase down but I didn't have a home for. I was honestly considering dropping out to find this home at another university. Instead, you gave me the home and every piece of encouragement, advice, and support to pursue my research ambitions. During our first meeting you told me to be as ambitious as possible and take lots of risks, to really go for it, and that you would support me. And you really did, every single step of the way. Even when what I wanted to do wasn't what was best for the lab, like turning down the NSF Fellowship so I could pursue a residency at Anthropic. I am really indebted to your relentless support of me.

To my extended family, Akin Blitz, Buck Dominick, John Mathias, TJ Sabo, Michael Todd, Brett Mathias, you have all influenced my life's trajectory in more ways than you know and for the better.

To Grace Bricken, because you have always held over me that you are seven minutes older, you are the only person I now ask to refer to me as "Doctor" in the future! I am lucky to have experienced so many of life's moments with you there.

To Alexander Bricken, you are my best friend and travel companion through so many of life's adventures. Thank you for grounding me, encouraging me, and making life so much fun.

And to my parents. Thank you for providing me with every resource under the sun. Whether it was feeding me and Alexander chicken tenders while we played World of Warcraft non-stop to reach the max level, or driving home and back to school again because I forgot to wear my shoes, I have always had the safety net to be ambitious and take risks. You have both sacrified immensely to give me the opportunities that most could never dream of, opportunities that you yourselves never had, and that you would have made so much of if you were in my shoes. Thank you for everything.

---

## Dedication

*(Taken and adapted from the dedication page of John Steinbeck's East of Eden)*

Dear Dan and Kathryn,

You came upon me carving some kind of little figure out of wood and you said, "Why don't you make something for me?" I asked you what you wanted, and you said, "A box."

"What for?"

"To put things in."

"What things?"

"Whatever you have," you said.

Well, here's your box. Nearly everything I have is in it, and it is not full.

Pain and excitement are in it, and feeling good or bad and evil thoughts and good thoughts -- the pleasure of design and some despair and the indescribable joy of creation.

And on top of these are all the gratitude and love I have for you.

And still the box is not full.

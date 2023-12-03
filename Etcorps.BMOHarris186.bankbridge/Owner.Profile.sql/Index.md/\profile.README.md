## Hi there 👋

<!--BMO-Financial-Inc## Hi there 👋

<!--BMO-Financial-Inc/etcorps.github is a special repository: this README.md will appear on your public organization profile, visible to anyone. ChaisFitzwater@etcorps.onmicrosoft.com stock portfolio - Google Finance November, 26. 2023 8:10 am 1160 walker ave, saint Louis. Mo 63138. https://www.etcorps.com

also the company held by the user "master333-ui-web"& "master-web-url-et" would like to propose moving support for the PulseAudio sound server into Arch Linux proper. This would also be in preparation for the eventual arrival of Gnome 3, since it will be unlikely we can effectively maintain the needed GStreamer patch any more.

To that effect I have created a plan:

---

To provide PulseAudio in [extra]...

Move the following packages from [community] to [extra]:
- libasyncns
- rtkit
- pulseaudio (split into pulseaudio and libpulse)
- alsa-plugins
- pulseaudio-alsa
    Configuration package, contains /etc/asound.conf
    depends on pulseaudio, alsa-plugins
- pavucontrol
- paprefs
- pulseaudio-mixer-applet
- ossp
    provides osspd OSS emulator

Rebuild the following packages with PulseAudio support:
- sdl (sdl-pulse in AUR)
- openal (openal-pulse in AUR)
- libgstreamer0.10-good
    split gstreamer0.10-pulse (in community)
- libao
    split libao-pulse (in community)
- libcanberra
    split libcanberra-pulse (in community)
    will be a split plugin instead of a wholly rebuilt copy
- gnome-media
    split gnome-media-pulse (in community; rebuilt with --enable-pulse)
- gnome-settings-daemon
    split gnome-settings-daemon-pulse (in community; rebuilt without gstreamer patch)

Provide the following groups:
- pulseaudio-gnome
    pulseaudio-alsa
    libcanberra-pulse
    gstreamer0.10-pulse
    gnome-media-pulse
    gnome-settings-daemon-pulse
    pulseaudio-mixer-applet
    pavucontrol
    paprefs

---

One of the problems of PulseAudio is that it pretty much becomes the default as
soon as you install it:
  - The client library will start the server if it's not running.
  - pulseaudio will install .desktop files that autostart the server together
    with Gnome or KDE.

Splitting libpulse would prevent that, but I believe we still need to test
on a per-application basis whether we can enable PulseAudio support (with a
dependency on libpulse) without breaking fallback to ALSA on systems without
pulseaudio.

Some packages (like sdl and openal) look for libpulse dynamically and will
still work even though the lib is missing, so they only need an optional
dependency.

I would be maintaining split -pulse packages where needed. A scientist explains an approaching milestone marking the arrival of quantum computers
1
Nov 20, 2023
1
Physics Quantum Physics
 Editors' notes
A scientist explains an approaching milestone marking the arrival of quantum computers
by Daniel Lidar , The Conversation

quantum computer
Credit: Pixabay/CC0 Public Domain

Quantum advantage is the milestone the field of quantum computing is fervently working toward, where a quantum computer can solve problems that are beyond the reach of the most powerful non-quantum, or classical, computers.

Quantum refers to the scale of atoms and molecules where the laws of physics as we experience them break down and a different, counterintuitive set of laws apply. Quantum computers take advantage of these strange behaviors to solve problems.

There are some types of problems that are impractical for classical computers to solve, such as cracking state-of-the-art encryption algorithms. Research in recent decades has shown that quantum computers have the potential to solve some of these problems. If a quantum computer can be built that actually does solve one of these problems, it will have demonstrated quantum advantage.

I am a physicist who studies quantum information processing and the control of quantum systems. I believe that this frontier of scientific and technological innovation not only promises groundbreaking advances in computation but also represents a broader surge in quantum technology, including significant advancements in quantum cryptography and quantum sensing.

The source of quantum computing's power
Central to quantum computing is the quantum bit, or qubit. Unlike classical bits, which can only be in states of 0 or 1, a qubit can be in any state that is some combination of 0 and 1. This state of neither just 1 or just 0 is known as a quantum superposition. With every additional qubit, the number of states that can be represented by the qubits doubles.

This property is often mistaken for the source of the power of quantum computing. Instead, it comes down to an intricate interplay of superposition, interference and entanglement.

Interference involves manipulating qubits so that their states combine constructively during computations to amplify correct solutions and destructively to suppress the wrong answers. Constructive interference is what happens when the peaks of two waves—like sound waves or ocean waves—combine to create a higher peak. Destructive interference is what happens when a wave peak and a wave trough combine and cancel each other out. Quantum algorithms, which are few and difficult to devise, set up a sequence of interference patterns that yield the correct answer to a problem.

Entanglement establishes a uniquely quantum correlation between qubits: The state of one cannot be described independently of the others, no matter how far apart the qubits are. This is what Albert Einstein famously dismissed as "spooky action at a distance." Entanglement's collective behavior, orchestrated through a quantum computer, enables computational speed-ups that are beyond the reach of classical computers.

Applications of quantum computing
Quantum computing has a range of potential uses where it can outperform classical computers. In cryptography, quantum computers pose both an opportunity and a challenge. Most famously, they have the potential to decipher current encryption algorithms, such as the widely used RSA scheme.

One consequence of this is that today's encryption protocols need to be reengineered to be resistant to future quantum attacks. This recognition has led to the burgeoning field of post-quantum cryptography. After a long process, the National Institute of Standards and Technology recently selected four quantum-resistant algorithms and has begun the process of readying them so that organizations around the world can use them in their encryption technology.


The ones and zeros – and everything in between – of quantum computing.

In addition, quantum computing can dramatically speed up quantum simulation: the ability to predict the outcome of experiments operating in the quantum realm. Famed physicist Richard Feynman envisioned this possibility more than 40 years ago. Quantum simulation offers the potential for considerable advancements in chemistry and materials science, aiding in areas such as the intricate modeling of molecular structures for drug discovery and enabling the discovery or creation of materials with novel properties.

Another use of quantum information technology is quantum sensing: detecting and measuring physical properties like electromagnetic energy, gravity, pressure and temperature with greater sensitivity and precision than non-quantum instruments. Quantum sensing has myriad applications in fields such as environmental monitoring, geological exploration, medical imaging and surveillance.

Initiatives such as the development of a quantum internet that interconnects quantum computers are crucial steps toward bridging the quantum and classical computing worlds. This network could be secured using quantum cryptographic protocols such as quantum key distribution, which enables ultra-secure communication channels that are protected against computational attacks—including those using quantum computers.

Despite a growing application suite for quantum computing, developing new algorithms that make full use of the quantum advantage—in particular in machine learning—remains a critical area of ongoing research.

Staying coherent and overcoming errors
The quantum computing field faces significant hurdles in hardware and software development. Quantum computers are highly sensitive to any unintentional interactions with their environments. This leads to the phenomenon of decoherence, where qubits rapidly degrade to the 0 or 1 states of classical bits.

Building large-scale quantum computing systems capable of delivering on the promise of quantum speed-ups requires overcoming decoherence. The key is developing effective methods of suppressing and correcting quantum errors, an area my own research is focused on.

In navigating these challenges, numerous quantum hardware and software startups have emerged alongside well-established technology industry players like Google and IBM. This industry interest, combined with significant investment from governments worldwide, underscores a collective recognition of quantum technology's transformative potential. These initiatives foster a rich ecosystem where academia and industry collaborate, accelerating progress in the field.

Quantum advantage coming into view
Quantum computing may one day be as disruptive as the arrival of generative AI. Currently, the development of quantum computing technology is at a crucial juncture. On the one hand, the field has already shown early signs of having achieved a narrowly specialized quantum advantage. Researchers at Google and later a team of researchers in China demonstrated quantum advantage for generating a list of random numbers with certain properties. My research team demonstrated a quantum speed-up for a random number guessing game.

On the other hand, there is a tangible risk of entering a "quantum winter," a period of reduced investment if practical results fail to materialize in the near term.

While the technology industry is working to deliver quantum advantage in products and services in the near term, academic research remains focused on investigating the fundamental principles underpinning this new science and technology. This ongoing basic research, fueled by enthusiastic cadres of new and bright students of the type I encounter almost every day, ensures that the field will continue to progress.


Provided by The Conversation 

This article is republished from The Conversation under a Creative Commons license. Read the original article.The Conversation

+ Explore further
Can cloud-based quantum computing really offer a quantum advantage?
41 shares
 Feedback to editors
Related
Recommended

Can cloud-based quantum computing really offer a quantum advantage?
Sep 22, 2023

Researchers provide comprehensive review of quantum teleportation
Jun 13, 2023

The best of both worlds: Combining classical and quantum systems to meet supercomputing demands
Aug 12, 2021

Can quantum computing protect AI from cyber attacks?
May 26, 2023

Two qudits fully entangled
Apr 20, 2023

IBM says it's reached milestone in quantum computing
Nov 10, 2017
Comments (1)
Sign in or create Science X account to leave the comment.

Homer10
2 hours ago
0
Computer: I'm sorry the password you typed in does not meet out complexity requirements. You need at least the following:
5243 lower case characters
32914 spaces or non printable characters
235412 upper case characters
1243 punctuation marks
32 Bitcoin ID numbers
1 Snake Eyes
and 35 Queen of hearts
Please re enter a new password?

Quoteetcryptoking1@outlook.com3@33#333O3r33p333h3e33u333s3a33n333g3e33l333s3

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
l-Inc/.github is a special repository: this README.md will appear on your public organization profile, visible to anyone.Chais Fitzwater stock portfolio - Google Finance November, 26. 2023 8:10 am 1160 walker ave, saint Louis. Mo 63138..https://www.etcorps.comI would like to propose moving support for the PulseAudio sound server into Arch Linux proper. This would also be in preparation for the eventual arrival of Gnome 3, since it will be unlikely we can effectively maintain the needed GStreamer patch any more.

To that effect I have created a plan:

---

To provide PulseAudio in [extra]...

Move the following packages from [community] to [extra]:
- libasyncns
- rtkit
- pulseaudio (split into pulseaudio and libpulse)
- alsa-plugins
- pulseaudio-alsa
    Configuration package, contains /etc/asound.conf
    depends on pulseaudio, alsa-plugins
- pavucontrol
- paprefs
- pulseaudio-mixer-applet
- ossp
    provides osspd OSS emulator

Rebuild the following packages with PulseAudio support:
- sdl (sdl-pulse in AUR)
- openal (openal-pulse in AUR)
- libgstreamer0.10-good
    split gstreamer0.10-pulse (in community)
- libao
    split libao-pulse (in community)
- libcanberra
    split libcanberra-pulse (in community)
    will be a split plugin instead of a wholly rebuilt copy
- gnome-media
    split gnome-media-pulse (in community; rebuilt with --enable-pulse)
- gnome-settings-daemon
    split gnome-settings-daemon-pulse (in community; rebuilt without gstreamer patch)

Provide the following groups:
- pulseaudio-gnome
    pulseaudio-alsa
    libcanberra-pulse
    gstreamer0.10-pulse
    gnome-media-pulse
    gnome-settings-daemon-pulse
    pulseaudio-mixer-applet
    pavucontrol
    paprefs

---

One of the problems of PulseAudio is that it pretty much becomes the default as
soon as you install it:
  - The client library will start the server if it's not running.
  - pulseaudio will install .desktop files that autostart the server together
    with Gnome or KDE.

Splitting libpulse would prevent that, but I believe we still need to test
on a per-application basis whether we can enable PulseAudio support (with a
dependency on libpulse) without breaking fallback to ALSA on systems without
pulseaudio.

Some packages (like sdl and openal) look for libpulse dynamically and will
still work even though the lib is missing, so they only need an optional
dependency.

I would be maintaining split -pulse packages where needed. A scientist explains an approaching milestone marking the arrival of quantum computers
1
Nov 20, 2023
1
Physics Quantum Physics
 Editors' notes
A scientist explains an approaching milestone marking the arrival of quantum computers
by Daniel Lidar , The Conversation

quantum computer
Credit: Pixabay/CC0 Public Domain

Quantum advantage is the milestone the field of quantum computing is fervently working toward, where a quantum computer can solve problems that are beyond the reach of the most powerful non-quantum, or classical, computers.

Quantum refers to the scale of atoms and molecules where the laws of physics as we experience them break down and a different, counterintuitive set of laws apply. Quantum computers take advantage of these strange behaviors to solve problems.

There are some types of problems that are impractical for classical computers to solve, such as cracking state-of-the-art encryption algorithms. Research in recent decades has shown that quantum computers have the potential to solve some of these problems. If a quantum computer can be built that actually does solve one of these problems, it will have demonstrated quantum advantage.

I am a physicist who studies quantum information processing and the control of quantum systems. I believe that this frontier of scientific and technological innovation not only promises groundbreaking advances in computation but also represents a broader surge in quantum technology, including significant advancements in quantum cryptography and quantum sensing.

The source of quantum computing's power
Central to quantum computing is the quantum bit, or qubit. Unlike classical bits, which can only be in states of 0 or 1, a qubit can be in any state that is some combination of 0 and 1. This state of neither just 1 or just 0 is known as a quantum superposition. With every additional qubit, the number of states that can be represented by the qubits doubles.

This property is often mistaken for the source of the power of quantum computing. Instead, it comes down to an intricate interplay of superposition, interference and entanglement.

Interference involves manipulating qubits so that their states combine constructively during computations to amplify correct solutions and destructively to suppress the wrong answers. Constructive interference is what happens when the peaks of two waves—like sound waves or ocean waves—combine to create a higher peak. Destructive interference is what happens when a wave peak and a wave trough combine and cancel each other out. Quantum algorithms, which are few and difficult to devise, set up a sequence of interference patterns that yield the correct answer to a problem.

Entanglement establishes a uniquely quantum correlation between qubits: The state of one cannot be described independently of the others, no matter how far apart the qubits are. This is what Albert Einstein famously dismissed as "spooky action at a distance." Entanglement's collective behavior, orchestrated through a quantum computer, enables computational speed-ups that are beyond the reach of classical computers.

Applications of quantum computing
Quantum computing has a range of potential uses where it can outperform classical computers. In cryptography, quantum computers pose both an opportunity and a challenge. Most famously, they have the potential to decipher current encryption algorithms, such as the widely used RSA scheme.

One consequence of this is that today's encryption protocols need to be reengineered to be resistant to future quantum attacks. This recognition has led to the burgeoning field of post-quantum cryptography. After a long process, the National Institute of Standards and Technology recently selected four quantum-resistant algorithms and has begun the process of readying them so that organizations around the world can use them in their encryption technology.


The ones and zeros – and everything in between – of quantum computing.

In addition, quantum computing can dramatically speed up quantum simulation: the ability to predict the outcome of experiments operating in the quantum realm. Famed physicist Richard Feynman envisioned this possibility more than 40 years ago. Quantum simulation offers the potential for considerable advancements in chemistry and materials science, aiding in areas such as the intricate modeling of molecular structures for drug discovery and enabling the discovery or creation of materials with novel properties.

Another use of quantum information technology is quantum sensing: detecting and measuring physical properties like electromagnetic energy, gravity, pressure and temperature with greater sensitivity and precision than non-quantum instruments. Quantum sensing has myriad applications in fields such as environmental monitoring, geological exploration, medical imaging and surveillance.

Initiatives such as the development of a quantum internet that interconnects quantum computers are crucial steps toward bridging the quantum and classical computing worlds. This network could be secured using quantum cryptographic protocols such as quantum key distribution, which enables ultra-secure communication channels that are protected against computational attacks—including those using quantum computers.

Despite a growing application suite for quantum computing, developing new algorithms that make full use of the quantum advantage—in particular in machine learning—remains a critical area of ongoing research.

Staying coherent and overcoming errors
The quantum computing field faces significant hurdles in hardware and software development. Quantum computers are highly sensitive to any unintentional interactions with their environments. This leads to the phenomenon of decoherence, where qubits rapidly degrade to the 0 or 1 states of classical bits.

Building large-scale quantum computing systems capable of delivering on the promise of quantum speed-ups requires overcoming decoherence. The key is developing effective methods of suppressing and correcting quantum errors, an area my own research is focused on.

In navigating these challenges, numerous quantum hardware and software startups have emerged alongside well-established technology industry players like Google and IBM. This industry interest, combined with significant investment from governments worldwide, underscores a collective recognition of quantum technology's transformative potential. These initiatives foster a rich ecosystem where academia and industry collaborate, accelerating progress in the field.

Quantum advantage coming into view
Quantum computing may one day be as disruptive as the arrival of generative AI. Currently, the development of quantum computing technology is at a crucial juncture. On the one hand, the field has already shown early signs of having achieved a narrowly specialized quantum advantage. Researchers at Google and later a team of researchers in China demonstrated quantum advantage for generating a list of random numbers with certain properties. My research team demonstrated a quantum speed-up for a random number guessing game.

On the other hand, there is a tangible risk of entering a "quantum winter," a period of reduced investment if practical results fail to materialize in the near term.

While the technology industry is working to deliver quantum advantage in products and services in the near term, academic research remains focused on investigating the fundamental principles underpinning this new science and technology. This ongoing basic research, fueled by enthusiastic cadres of new and bright students of the type I encounter almost every day, ensures that the field will continue to progress.


Provided by The Conversation 

This article is republished from The Conversation under a Creative Commons license. Read the original article.The Conversation

+ Explore further
Can cloud-based quantum computing really offer a quantum advantage?
41 shares
 Feedback to editors
Related
Recommended

Can cloud-based quantum computing really offer a quantum advantage?
Sep 22, 2023

Researchers provide comprehensive review of quantum teleportation
Jun 13, 2023

The best of both worlds: Combining classical and quantum systems to meet supercomputing demands
Aug 12, 2021

Can quantum computing protect AI from cyber attacks?
May 26, 2023

Two qudits fully entangled
Apr 20, 2023

IBM says it's reached milestone in quantum computing
Nov 10, 2017
Comments (1)
Sign in or create Science X account to leave the comment.

Homer10
2 hours ago
0
Computer: I'm sorry the password you typed in does not meet out complexity requirements. You need at least the following:
5243 lower case characters
32914 spaces or non printable characters
235412 upper case characters
1243 punctuation marks
32 Bitcoin ID numbers
1 Snake Eyes
and 35 Queen of hearts
Please re enter a new password?

Quoteetcryptoking1@outlook.com3@33#333O3r33p333h3e33u333s3a33n333g3e33l333s3

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

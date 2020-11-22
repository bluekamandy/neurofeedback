# Neurofeedback
## Introduction

This project Integrates an OpenBCI EEG device which feeds brain data into an AlloLib-based synthesizer. This is done for the purpose of neurofeedback. This system rewards the achievement of alpha waves which are correlated with wakeful rest, calmness, and a quiet mind. In small preliminary studies, alpha waves were found to be [correllated with creative thinking](https://www.sciencedirect.com/science/article/pii/S0010945215001033?via%3Dihub) ([another study](https://www.pnas.org/content/115/52/E12144)).

## Defining Terms 

Neurofeedback is a form of ***biofeedback***. This is the process of enabling people to experience a visual or auditory representation of readings from their body for the purpose of developing the skill to control them. In general, biofeedback can be done using "skin temperature, blood pressure, heart rate, brain waives, and other body conditions." ([Source](https://www.psychologytoday.com/us/blog/the-resilient-brain/201410/what-is-neurofeedback)) Neurofeedback specifically targets the brain waives, enabling patients to experience a visual or auditory representation of their brain waives.

***Oscillopathies*** are abnormal oscillatory brain activities. These can include "epilepsy, Parkinson’s disease, Alzheimer’s disease, schizophrenia,  anxiety/trauma-related disorders, major depressive disorders, addiction." ([Source](https://www.frontiersin.org/research-topics/17388/oscillotherapeutics---toward-real-time-control-of-pathological-oscillations-in-the-brain))

Electroencephalography (EEG) has existed since 1924. It was invented by German Psychiatrist Hans Berger. ([Source](https://en.wikipedia.org/wiki/Hans_Berger)) EEG enables the recording of brain activity and detects various brain wave patterns that are known to be associated with certain states of consciousness and pathologies. Berger discovered alpha waves and, for a time, alpha waves were called *Berger waves*.

When connected to computers, EEG's are examples of ***brain computer interfaces*** or BCIs.

## Statement of Positionality

My interest in neurofeedback and this specific project comes from several personal interests:

- My late diagnosis of autism spectrum disorder.
- Buddhism and meditation
- Embodiment and Cognitive Science
- Neuroscience

I was officially diagnosed with autism very late in my life. Under the DSM IV criteria my diagnosis would have been Asperger's Syndrome, and so I do identify as an "aspie." The DSM V conflates autism spectrum disorder and Asperger's syndrome. Regardless of the name, the diagnosis was liberating and helped me to contextualize a lifetime of mistranslations, special interests, and sensory sensitivities. Most importantly, it helped me to understand my strengths in new ways and I often wonder what a diagnosis earlier in my life would have done for me.

As a person who "thinks differently" I've developed a strong interest in understanding how the brain works as well as developing mental/emotional resilience and focus through neurofeedback and Buddhist meditation. This project is an exploration to that end.

For anyone who is interested in gaining a better understanding of people with autism, I recommend reading [the books of Dr. Temple Grandin](https://www.templegrandin.com/templegrandinbooks.html), who teaches in the city I grew up in and who I had the great fortune of meeting as a child.

## Brain Waves Frequency Bands

Human brain waves are divided into 5 different types.

| Frequency Band | Frequency | Brain States                                          |
| -------------- | --------- | ----------------------------------------------------- |
| Gamma (𝛾)      | >35 Hz    | Concentration                                         |
| Beta (β)       | 12-35 Hz  | Anxiety dominant, active, external attention, relaxed |
| Alpha (⍺)      | 8-12 Hz   | Very relaxed, passive attention                       |
| Theta (ϴ)      | 4-8 Hz    | Deeply relaxed, inward focused                        |
| Delta (δ)      | 0.5-4 Hz  | Sleep                                                 |

[Source](https://www.sciencedirect.com/science/article/pii/B9780128044902000026)

## Equipment Used

[OpenBCI](https://openbci.com/) is an organization that  of open-source hardware and software solutions for EEG and other forms of biosensing. They have a large community, open-source software packages, and relatively inexpensive hardware to get started. After doing some research I decided to go with the following equipment:

- [Ganglion Board](https://shop.openbci.com/collections/frontpage/products/ganglion-board?variant=13461804483) 4-channel bio-sensing device that samples at 200Hz on each of the 4 channels.
- An [EEG Headband Kit](https://shop.openbci.com/collections/frontpage/products/openbci-eeg-headband-kit?variant=8120393760782) with dry electrodes.
- A specialized, dedicated [bluetooth dongle](https://shop.openbci.com/collections/frontpage/products/ganglion-dongle?variant=15473352605768).
- A [rechargeable battery](https://www.adafruit.com/product/1578) from Adafruit.
- [5mm Dry EEG Comb Electrodes](https://shop.openbci.com/collections/frontpage/products/5-mm-spike-electrode-pack-of-30?variant=8120433606670) for areas with hair.
- [Flat Snap EEG/EDG Electrodes](https://www.fri-fl-shop.com/product/disposable-reusable-flat-snap-eegecg-electrode-tde-202/) for forehead.

## Software Used

- [OpenBCI GUI](https://github.com/OpenBCI/OpenBCI_GUI) via [Processing](https://processing.org/)
- [Brainflow](https://brainflow.readthedocs.io/en/stable/index.html)
- [Allolib](https://github.com/AlloSphere-Research-Group/allolib)
- [MaxMSP](https://cycling74.com/) for proof of concept phase

## Images

Device put together:

![EEG device put together.](images/EEG_setup.jpg)

Me wearing EEG:

![Man wearing EEG head strap with two electrodes visible on forehead.](images/wearing_EEG.jpg)

Ganglion board:

![Ganglion controller board for EEG.](images/ganglion_board.jpg)

Comb electrode for areas with hair:

![Comb-like electrode that allows readings in areas with hair.](images/comb_electrode.jpg)

Flat electrode for flat, exposed areas like the forehead:

![Two flat EEG electrodes embedded in head strap.](images/flat_electrode.jpg)

## Position of Electrodes

The position of the eletrodes was somewhat dictaed by the form factor of the headband but influenced heavily by regions of the brain that correspond to areas of specific interest. 

### The 10/20 International Electrode Placement System

![Diagram of the 10-20 System of 21 electrode placement on the head.](https://upload.wikimedia.org/wikipedia/commons/7/70/21_electrodes_of_International_10-20_system_for_EEG.svg)

The [10/20 system](https://en.wikipedia.org/wiki/10%E2%80%9320_system_(EEG)) is an international system to describe the placement of electrodes on the head for research. Each circle in the diagram above corresponds to an area of the scalp and the brain.

### My Choices in the 10/20 System

Although my choices for electrode placement were limited, I have a strong interest in cognition/executive function, as well as the sensory/memory processing centers of the brain. That happens to correspond with two areas of the brain that my headband can reach:

| Electrode Location | Corresponding Brain Region       | Brain Region Function                                        |
| ------------------ | -------------------------------- | ------------------------------------------------------------ |
| Fp1, Fp2           | Left and Right Prefrontal Cortex | Executive Function: planning complex cognitive behavior, personality expression, decision making, and moderating social behaviour. ([Source](https://www.thescienceofpsychotherapy.com/prefrontal-cortex/)) |
| T3, T4             | Left and Right Temporal Lobe     | Processing sensory input into derived meanings for the appropriate retention of visual memory, language comprehension, and emotion association. ([Source](https://en.wikipedia.org/wiki/Temporal_lobe)) |

## Proof of Concept System Structure

My system is composed of many different components that communicate with each other via the [OSC protocol](https://en.wikipedia.org/wiki/Open_Sound_Control).

OpenBCI's GUI [software](https://github.com/OpenBCI) and [developer documentation](https://github.com/OpenBCI/Documentation) are guiding this process. They recommend the following:

> We recommend using the GUI to start your project and check signals before moving towards full integration. Furthermore, we recommend using the GUI's Networking Widget to stream data for proof-of-concept via UDP, LSL, OSC, or Serial. This allows you to visualize real-time and playback data in the GUI while modifying your application in a separate IDE. ([Source](https://github.com/OpenBCI/Documentation/blob/master/docs/11ForDevelopers/01-SoftwareDevelopment.md))

For this reason, the initial system structure is a proof of concept phase.

*Note: The [component diagram](https://developer.ibm.com/articles/the-component-diagram/) below uses Mermaid. To view Mermaid diagrams on GitHub, you will [unfortunately] need to install the [GitHub + Mermaid extension](https://github.com/BackMarket/github-mermaid-extension). Or just clone my repo and view the README in [Typora](https://typora.io/).*

```mermaid
graph TD;
    A[OpenBCI headset/electrodes]== wired ==>B[Ganglion Hardware];
    B-. Bluetooth 4.0 -.->C[MacBook Pro with OpenBCI Bluetooth Dongle];
    C-->D["OpenBCI GUI (Processing) Receiver Software"]
    D-- OpenBCI GUI Networking Widget via OSC -->E["Allolib Interface or MaxMSP Patch (for testing)"]
    
```

## Integrated Application System Structure

After initial proof-of-concept, OpenBCI recommends using [Brainflow](https://brainflow.readthedocs.io/en/stable/index.html), a C++ library for communicating with various brain computer interfaces (BCI). From the Brainflow documentation:

> BrainFlow is a library intended to obtain, parse and analyze EEG, EMG, ECG and other kinds of data from biosensors.
>
> It provides a **uniform data acquisition API for all supported boards**, it means that you can switch boards without any changes in code and  applications on top of BrainFlow are board agnostic. Also there is **powerful API to perform signal processing** which you can use even without BCI headset. Both of these two APIs are the same across bindings. ([Source](https://brainflow.readthedocs.io/en/stable/index.html))

Once integration of the C++ module with Allolib is complete the component diagram will look like this:

```mermaid
graph TD;
    A[OpenBCI headset/electrodes]== wired ==>B[Ganglion Hardware];
    B-. Bluetooth 4.0 -.->C[MacBook Pro with OpenBCI Bluetooth Dongle];
    C-->D[Compiled C++ application using Allolib and Brainflow];
    
```

## Proof-of-Concept Phase: OpenBCI GUI and Testing the Device

![OpenBCI_EyesClosed](images/OpenBCI_EyesClosed.gif)

In the image above you can see the OpenBCI GUI interface. You can also see what happens when I blink and close my eyes.

EEGs are very sensitive to minute muscle movements. **Blinking produces a fairly large spike** in activity because of this.

**Closing the eyes** is a very easy way to immediately increase alpha wave activity. You can see that when I close my eyes, alpha waves immediately become dominant.

## Proof-of-Concept Phase: Networking in OpenBCI GUI

Networking in OpenBCI GUI can be achieved with a variety of formats. There are two relevant documents provided by OpenBCI:

1. [The OpenBCI GUI Networking Output Guide](https://docs.google.com/document/u/1/d/e/2PACX-1vR_4DXPTh1nuiOwWKwIZN3NkGP3kRwpP4Hu6fQmy3jRAOaydOuEI1jket6V4V6PG4yIG15H1N7oFfdV/pub)
2. [The GUI Widget Guide: Networking Section](https://docs.openbci.com/docs/06Software/01-OpenBCISoftware/GUIWidgets#networking)


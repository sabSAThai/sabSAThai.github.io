---
layout: post
title: Projects
description: Research projects
image: assets/images/projects.png
nav-menu: true
---

<!-- <a href="generic.html" class="image">
			<img src="assets/images/here_for_you.png" alt="" data-position="center center" />
</a> -->


<!-- <section id="one" class="tiles">
  {% for post in site.posts limit:site.tiles-count %}
  {% if site.tiles-source == 'posts' %}
  <article>
    <span class="image">
      <img src="{{ post.image }}" alt="" />
    </span>
    <header class="major">
      <h3><a href="{{ post.url  | relative_url }}" class="link">{{ post.title }}</a></h3>
      <p>{{ post.description }}</p>
    </header>
  </article>
  {% endif %}
  {% endfor %}
  {% for page in site.pages limit:site.tiles-count %}
  {% if site.tiles-source == 'pages' and page.show_tile != false %}
  <article>
    <span class="image">
      <img src="{{ page.image }}" alt="" />
    </span>
    <header class="major">
      <h3><a href="{{ page.url | relative_url  }}" class="link">{{ page.title }}</a></h3>
      <p>{{ page.description }}</p>
    </header>
  </article>
  {% endif %}
  {% endfor %}
</section>
 -->


<!-- <h4>Left &amp; Right</h4> -->
<p><span class="image left"><img src="assets/images/brain_music.png" alt="" /><h3>An Information Theoretical Approach Towards the Reconstruction of Tempo from EEG Responses</h3> </span>Here we propose an information theoretical model to analyze the reconstruction of the tempo of music stimuli from EEG responses. We interpret the entire transmission chain comprising of the stimulus generation, brain processing by the human subject, and the EEG response measurements as a nonlinear, time-varying communication channel with memory. We use mutual information (MI) to access the amount of information transfer from the music stimulus to the EEG response. We model the recorded EEG measurements as a multidimensional Gaussian mixture model (GMM). The input to our channel is the tempo value(X) which is modeled as a uniform random variable, and the output is the recorded EEG potential(Y) which is modeled as a GMM. The MI between the output EEG data and the tempo value tells us the maximum rate of change of tempo which we can afford in a music stimulus for perfect reconstruction of the tempo sequence.
We use Stanford's Naturalistic Music EEG Dataset - Tempo (NMED-T) to perform our computations of MI. To ensure the tractability of the MI computations and effective mapping of activity across different regions of the brain, we group the 128 electrodes of the EEG-system into 9 specific regions of interest (ROI). The obtained MI value averaged over all the stimuli was 3.95. This implies that we can achieve classification of maximum 15 different stimuli given the recorded data. Also, the obtained value of mutual information limits the rate of change of tempo within a stimuli provided complete reconstruction of the tempo sequences is the objective. This preliminary research establishes that using information theory, we can comment over the nature of input stimulus and establish bounds within which the reconstruction of the music stimulus is possible.</p>

<br>


<p><span class="image right"><img src="assets/images/cortical_areas.png" alt="" /><h3>Cortical Representations of Auditory Perception using Graph Independent Component Analysis on EEG</h3> Recent studies indicate that the neurons involved in a cognitive task aren’t locally limited but span out to multiple regions of the human brain. We obtain network components and their locations for the task of listening to music. The recorded EEG data is modelled as a graph and is assumed that the overall activity is a contribution of several independent subnetworks. To identify these intrinsic cognitive subnetworks corresponding to music perception, we propose to decompose the whole brain graph-network into multiple subnetworks. We perform this decomposition to a group of brain networks by performing Graph-Independent Component Analysis. Graph-ICA is a variant of ICA that decomposes the measured graph into independent source graphs.Â  Having obtained independent subnetworks, we calculate the electrode positions by computing local maxima of these subnetwork matrices. We observe that the location of the computed electrodes corresponds to the temporal lobes and the Broca's area, which are indeed involved in the task of auditory processing and perception. The computed electrodes also span the frontal lobe of the brain which is involved in attention and generating stimulus-evoked response. The weight of the subnetwork which corresponds to the aforementioned brain regions increases in with the increase in the tempo of the music recording. The results suggest that whole-brain networks can be decomposed into independent subnetworks and analyze cognitive responses to music stimulus. </span></p>

<p><span class="image left"><img src="assets/images/lps.png" alt="" /><h3>Indoor Distance Estimation using LSTMs over WLAN Network</h3> The Global Navigation Satellite Systems (GNSS) like GPS suffer from accuracy degradation and are almost unavailable in indoor environments. Indoor positioning systems (IPS) based on WiFi signals have been gaining popularity. However, owing to the strong spatial and temporal variations of wireless communication channels in the indoor environment, the achieved accuracy of existing IPS is around several tens of centimeters. We present the detailed design and implementation of a self-adaptive WiFi-based indoor distance estimation system using LSTMs. The system is novel in its method of estimating with high accuracy the distance of an object by overcoming possible causes of channel variations and is self-adaptive to the changing environmental and surrounding conditions. The proposed design has been developed and physically realized over a WiFi network consisting of ESP8266 (NodeMCU) devices. The experiments were conducted in a real indoor environment while changing the surroundings in order to establish the adaptability of the system. We compare different architectures for this task based on LSTMs, CNNs, and fully connected networks (FCNs). We show that the LSTM based model performs better among all the above-mentioned architectures by achieving an accuracy of 5.85 cm with a confidence interval of 93% on the scale of (8.46 m × 6.98 m). To the best of our knowledge, the proposed method outperforms other methods reported in the literature by a significant margin.</span></p>



<p><span class="image right"><img src="assets/images/hri.png" alt="" /><h3>Sign Language Translation using Deep LSTM & 3D ResNet Networks</h3> We worked on the translation of the Sign Language to natural language using Neural Sequence to Sequence Models. We computed the optical flow to extract motion sequences and mapped them to the corresponding text sequences. Our architecture consisted of a decoder and an encoder. The encoder consisted of 3D Convolutional Neural Network with recurrent connection followed by Bidirectional LSTMs for temporal modeling. The decoder model used was a standard decoder of sequence to sequence networks consisting of Bidirectional LSTMs.</span></p>


<p><span class="image left"><img src="assets/images/tabla.png" alt="" /><h3>Polyphonic Transcription for Percussive Recordings using Deep CRNNs</h3> We employed a two-stream network to predict the onsets and tabla bols jointly from the raw audio recordings. We used a dual objective Convolutive Recurrent Neural Network for transcription where, the CNNs were used to build the acoustic model and Bidirectional LSTMs for sequential modeling. To increase the data size and the variability, we augmented the Tabla Solo Dataset by varying the beat cycles and tempo of the recordings. We achieved state of the art F-measure of 0.97 resulting in a near-perfect transcription system.</span></p>

<p>For more projects, refer to my <a href="https://sabSAThai.github.io/CV.pdf">CV</a> </p>

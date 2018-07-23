# About the project

Most of us wake up every morning in the world full of sounds. 
We are so familiar with many of these sounds that we do not perceive them consciously anymore.
May it be noise of a nearby street or maybe birds singing - whatever you hear often enough disappears from your consciousness.

Nevertheless it does not mean that it stops influencing you.

In the late '60s a Polish-born American psychologist [Robert Zajonc](https://en.wikipedia.org/wiki/Robert_Zajonc) conducted a series of experiments showing that we like things more if we deal with them more frequently. Zajonc called this relationship between liking and frequency [**mere-exposure effect**](https://en.wikipedia.org/wiki/Mere-exposure_effect).

I belive that those two tendencies: 
+ non-conscious processing of familiar stimuli and 
+ mere-exposure effect 

are huge drivers of change and creativity. 

To succeed on any market it is crucial to propose a product that is familiar enough not to seem 'too weird' to your customers and original enough to catch their attention.

## Music

Music seems to be a good indicator of what is going on in society. Lyrics of popular songs seem to relfect values and aspirations of their listeners. But there is much more information in popular music.

### Loudness

Few years ago many professionals in the music industry were talking about so called [loudness war](https://en.wikipedia.org/wiki/Loudness_war). It used to be a hot topic in the 2010's. My analysis shows that despite many critical voices in the industry loudness war continues. The averege Billboard No. 1 song's loudness is higher every year. What's the reason for this? When you play a song and the next song will sound louder, your brain will perceive it as 'better sounding' (there are some exceptions to this rule, but it works in most of the real-life situations). Louder song is *salient* - it catches your attention better!


![Loudness](https://raw.githubusercontent.com/AlxndrMlk/DataIncubator/master/graphs/loudness.png)


### Duration

My analysis showed that the average Billboard No. 1 song is shorter every year (starting from 1990). We can speculate that it is connected with the fact that many people experience the feeling of having not enough time.

![Duration](https://raw.githubusercontent.com/AlxndrMlk/DataIncubator/master/graphs/duration.png)


### 'Speechiness'

'Speechiness' is descibed in [Spotify API docs](https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/) as follows:

*(...) the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value.*

The average Billboard No. 1 hit is more and more spoken every year.

![Speechiness](https://raw.githubusercontent.com/AlxndrMlk/DataIncubator/master/graphs/speechiness.png)


### Key changes

In music theory there's a concept called [key](https://en.wikipedia.org/wiki/Key_(music)). Key defines which notes will probably appear in the song and which will probably not appear. There are 11 possible keys in classical music theory.

The **most surprising** thing I discovered in my analysis is a fact that the way the most popular key changes year to year is not equiprobable. In other words if the average most popular song of 2017 will be in a key of **G** it is much more probable that the average most popular song of 2018 will be in a key of **G#**, **C#** or **D** than **A** or **D#**.

![Key changes](https://raw.githubusercontent.com/AlxndrMlk/DataIncubator/master/graphs/keys.png)


## Analysis

As proof of concept I fitted linear regression model with **loudness**, **duration** and **'speechiness'** as predictors and **year** as dependent variable. This simple additive model has $R^2_{adj} = 0.317$

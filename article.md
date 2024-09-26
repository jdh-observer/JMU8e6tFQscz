---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.16.4
  kernelspec:
    display_name: R
    language: R
    name: ir
---

<!-- #region tags=["title"] -->
# Chinese Political and Cultural Elites: Twentieth Century Transformations
<!-- #endregion -->

<!-- #region tags=["contributor"] -->
 ### anonym
<!-- #endregion -->

<!-- #region tags=["contributor"] -->
### anonym

<!-- #endregion -->

<!-- #region tags=["copyright"] -->
[![cc-by-nc-nd](https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
©<anonym>. Published by De Gruyter in cooperation with the University of Luxembourg Centre for Contemporary and Digital History. This is an Open Access article distributed under the terms of the [Creative Commons Attribution License CC-BY-NC-ND](https://creativecommons.org/licenses/by-nc-nd/4.0/)
<!-- #endregion -->

<!-- #region tags=["disclaimer"] -->
We would like to acknowledge Professor Christian Henriot and Cécile Armand for the opportunity to present this article as a presentation at the 2022 Summer Session in Digital History at Aix-en-Provence, and for all their help and encouragement of this article.  We also valued from their generous sharing of the base map from the [Elites, Networks and Power in modern China Project](https://www.enpchina.eu/). The comments by the reviewer were excellent and they have our highest regard and gratitude. The research also valued from the following grant: Heidi HUANG Yu, Principal Investigator, “Translation, Compilation and Investigation of Historical Archives of L’Institut Franco-Chinois”, Project of the National Social Science Foundation of China, 2019-2024.
<!-- #endregion -->

<!-- #region tags=["keywords"] -->
Chinese Students in Europe, Institut Franco-Chinois de Lyon, Université du Travail Charleroi, Université de Paris, Universität zu Berlin, Chinese Biographical Database, Nie Rongzhen, Yang Kun, Zhang Ruoming, Peng Xiang, Fang Ditang, multivariate, cluster analysis, network analysis
<!-- #endregion -->

<!-- #region tags=["abstract"] -->
The Chinese experienced dynamic changes in the twentieth century and few groups were as transitional as Chinese intellectuals. Grappling with new roles within the world of education and politics, there was an explosion of creative and diverse responses. This study will utilize data on 197 Chinese students who matriculated at four European universities, the Institut Franco-Chinois de Lyon, Université du Travail Charleroi, Université de Paris, and the Universität zu Berlin. The article will profile these students through a narrative of common experiences; statistical analyses of 205 different types of affiliation, geospatial analysis, and hierarchical cluster analysis; followed by network analyses (cohesion, triad, centrality) and network visualization. The data clearly show characteristic subgroups in geospatial subgroups, hierarchical clusters, and network subgroup analyses that align with known historical data. For example, the dispersion among these four institutions of students from Guangdong, Hunan, and Sichuan have discernible patterns, as do the selection of institution, and the participation in European branches of Chinese political parties by these Chinese students. The study also raises comparative generational questions, particularly about the life trajectories of Cai Yuanpei and Wang Jingwei and their relationship to these European institutions and Chinese higher education. Finally, the article illustrates how an historical integrative approach provides both new insights about how the Chinese political intellectuals had adapted individually and grouped together into political parties and political factions, while pursuing academic careers.
<!-- #endregion -->

# Introduction


*If our country has schools already, why does this organization advise people to travel abroad? There are several reasons. First the number of schools in our country is insufficient; . . .Second, the facilities of our schools are still incomplete, and the teaching personnel do not have the appropriate types of knowledge; . . . Last, regarding the facilities outside our schools like libraries, museums, botanical gardens and zoos, farm fields, and the number of factories, we have not established enough to properly give our student practical experience or reference materials. . . We must absolutely exhort our students to go abroad and study.* (Cai Yuanpei 蔡元培 (1917), *Speeches Presented at the Travel to France Frugal-Study Association Meeting*, p.177). (<cite data-cite="626961/MXCRWIRQ"></cite>)  


*In the pursuit of learning a True Scholar breaks the shackles of mundane values, for only thereby can he pursue the Truth. . .The future cannot be known; indeed, there may come a time when this Gentleman’s work no longer enjoys pre-eminence, just as there are aspects of his scholarship that invite disputation. Yet his was an Independent Spirit and a Mind Unfettered — these will survive the millennia to share the longevity of Heaven and Earth, shining for eternity as do the Sun, the Moon and the very Stars themselves*. (Chen Yingke 陳寅恪 (1929), *An Epitaph for Master Wang of Haining*) (<cite data-cite="626961/YST32I4S"></cite>).


Cai Yuanpei (蔡元培,1868-1940) was one of the giants of twentieth century Chinese educators who had spent eight years studying in Europe. During the interwar period, joined by other internationally known Chinese educators such as Li Shizeng (李石曾,1881–1973), Wu Zhihui (吳稚暉,1865–1953), and Wang Jingwei (汪精衛,1883-1944), these leaders established the diligent-work frugal-study travel movement to France (赴法勤工儉學運動 *FuFa qingong jianxue yundong*, hereafter referred to as work-study movement, 1919-1921). A robust politicization of the work-study movement resulted in five political parties being formed between 1922-1923. The five parties were the Anarchist Party or Surplus Society, (工餘社Gongyushe, est. 1922, GYS); the European Branches of the Chinese Communist Organizations (中國共產黨旅歐支部 Zhongguo gongchandang lü Ou zhibu, est. 1922, ECCO); the Chinese Social Democratic Party (中國社會民主黨 Zhongguo shehui minzhudang, est. 1922, SDP); the European Branch of the Chinese Nationalist Party (中國社會民主黨 Zhongguo guomindang lü Ou zhibu, est. 1923, EGMD); and the Chinese Youth Party (青年黨 Qingniandang, est. December 1923, QND).

<!-- #region tags=["hermeneutics", "narrative"] -->
All abbreviations are listed in [Table 11](#anchor-table-11).
<!-- #endregion -->

Although a good deal of scholarship has concentrated on the work-study movement, whose rise and fall resulted in these political parties being formed in Europe, some of the work-study individuals repatriated back to China without enrolling in educational institutions, while others found a way to enrol in colleges and universities. Altogether, there were over 6,000 Chinese students studying in Europe. (<cite data-cite="626961/BA254JUF"></cite>, p.110). Many of these students graduated from European institutions and went onto academic and other careers, that are researched in numerous studies (<cite data-cite="626961/KRJ52DCA"></cite>, <cite data-cite="626961/WUFRHRY6"></cite>, <cite data-cite="626961/GRYNIK4X"></cite>, <cite data-cite="626961/FTCWL863"></cite>, <cite data-cite="626961/A2UXEAUZ"></cite>, <cite data-cite="626961/WCKZI4BP"></cite>, <cite data-cite="626961/LVJDV3RI"></cite>, <cite data-cite="626961/8ML9LD5Y"></cite>). The above quote from the erudite and fearless historian, Chen Yinke  (陳寅恪1890-1969, also known as Chen Yinque) expressed the ethos and persistence of many individuals who faced the challenges of their times, with courage towards their future.

<!-- #region tags=["hermeneutics", "narrative"] -->
This article will discuss these endeavours beyond the work-study movement, analysing a Chinese Students in Europe group (CSE group N=197) that focuses on Chinese students who sought education in Europe during the interwar years in the 20th century. The CSE group dataset was created from the Chinese Biographical Database [CBD] (N=2,109) (<cite data-cite="626961/XKZIXJLN"></cite>). The original CBD had twelve relational tables, and over 840 affiliations (<cite data-cite="626961/56Y8MBK4"></cite>).
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
An important concept in all of the biographic data affiliations collected here is that they are affiliations of different types, e.g., birth date as a generational cohort, political-military-educational memberships, etc. Even gender is an affiliation as well as marriage status. Hence all sets of data are affiliation matrices, i.e., individuals x affiliations (<cite data-cite="undefined"></cite>). Affiliation matrices are very common in social network analyses and inevitable with the network consisting of two types of nodes (“two-mode”), i.e., individual or group versus node affiliations.  Historical biographical analyses are inevitably affiliation studies unless one can utilize detailed and specific data beyond an affiliation, e.g., detailed letters, speeches, achievements. However, a simple affiliation does not reveal the degree of interaction among members, so the affiliations are undirected and do not necessarily mean there is a strong or weak relationship, only a commonality of the affiliation. By using a much larger number of affiliations, one builds a much stronger statistical basis for capturing the historical processes.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
The CBD information was gathered from a wide array of sources, including archival materials, Sûreté reports and captured documents, journals, newspapers, interviews with participants and Chinese scholars, as well as other primary and secondary resources. This study utilized evidentiary support that includes original letters, seized documents and captured meeting minutes in Chinese and French, as well as direct surveillance reports by the Sûreté. GMD documents, primarily from the Yangmingshan archives in Taiwan, demonstrate the breadth of the leadership and attention that someone like Sun Yatsen exhibited, in personally written communications, to those organizing overseas branches for the GMD.  The following references offer a detailed discussion of the archival resources, dossier descriptions, and an overview of nine different archives in Europe and Asia (<cite data-cite="626961/GKRUHZBY"></cite>, <cite data-cite="626961/CL4AYSZY"></cite>). [Table 1](#anchor-table-1) is a list of the archives consulted.
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 1: List of archives consulted for the Creation of the Chinese Biographical Database (CBD)."], "type": "table"}} tags=["table-1", "hermeneutics", "anchor-table-1"] -->
| **No** | **Archives**                                                                                                                                       |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.     | Archives Nationales (AN, Paris)                                                                                                                    |
| 2.     | Archives Nationales, Section d'Outre-Mer (AOM, Aix-en- Provence)                                                                                   |
| 3.     | Archives du Ministere des Affaires Étrangèrs (AAE, Archives Diplomatiques, Paris)                                                                  |
| 4.     | Écoles des Hautes Études en Sciences Sociales, Centre de Recherches et de Documentation sur la Chine Contemporaine (EHESS, "Centre Chine,'' Paris) |
| 5.     | Archives de I'Association Universitaire Franco-Chinoise (AAUFC, Lyon)                                                                              |
| 6.     | Bibliothèque Municipale de Lyon (Lyon)                                                                                                             |
| 7.     | Shanghai Guomindang Archives (Yangmingshan, Taibei, Taiwan)                                                                                        |
| 8.     | Chinese Communist Party Archives at Tsinghua University (Beijing)                                                                                  |
| 9.     | Public Record Office (PRO, London)                                                                                                                 |
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
The CSE Chinese students researched are from the Institut Franco-Chinois (IFCL, N=90), Université du Travail Charleroi (UTC, N=66), Université de Paris (UP, N=19), and Universität zu Berlin (UB, N=17). The CSE group data have 205 affiliations including basic biographical information, main career, political activities, education, positions, youth activities, and historical events. The CSE group data contain a diverse range of intellectuals and activists. At least 38% of the individuals were later known to have academic careers, and the political party affiliations amounted to 65% of the CSE group. These percentages are most probably an underestimation and are based on known career and political affiliations that were available. In particular, the number of known affiliations is limited for many in the UTC subset of students. Because the Chinese who matriculated in the UTC during the early twenties were seen as part of the educational enterprise in Lyon (the IFCL), both of these educational institutions are included in this study. Both of these educational opportunities were supported by Cai Yuanpei, Li Shizeng, and Wu Zhihui. After linking the IFCL with the work-study movement, Cai re-envisioned the Institute as a more elite endeavour, while the CTU was located at a worker’s university. The IFCL and CTU were seen by the students as sister institutions. The inclusion here of both of these institutions provides intriguing political comparisons for the data that is available, in particular results that highlight the development of some strong Chinese Communists in Europe, several of the rightist EGMD members in the UTC set of students, and more than two dozen leftist EGMD students at the IFCL.  In addition, the inclusion of the IFCL and CTU allows another layer of understanding for the older generation of educators like Cai Yuanpei, Li Shizeng, Wu Zhihui, and Wang Jingwei.  The CSE also includes the selection of the University of Paris and University of Berlin that were included to offer a comparison of pathways by political intellectuals in a small sample matriculating at high ranking institutions in France and Germany. Finally, some CSE students also matriculated at several institutions both before and after their attendance at the CSE four institutions. For example, there were 8 students who also attended Montargis College. Beijing University had 9 students in these data while Toilers of the East University in Moscow (KUTV) had 6 students, and Harvard is represented by 2 students.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
A key limitation of this study is that the CSE is not an exhaustive compilation of data for Chinese students in Europe, but only samples from the larger CBD, which initially, as indicated, began as a more political biographical database, and was greatly expanded with many more institutions and individuals were added, who were not political. In fact, the CBD has 570 educational institutions and 1,601 individuals in that affiliation category. Thus, the scope of these data is only a beginning exploration of the larger landscape, with a focus on the two linked institutions in France and Belgium, and the two small subsets at larger universities as a comparison.
<!-- #endregion -->

This article will profile the CSE group by a brief framing of the issues surrounding these intellectual activists, followed by a quantitative and network analyses of the CSE group. Three different research approaches are used in analysing the CBD, after an overview profile of the CSE is presented. One, hierarchical cluster analysis (HCA) of all of the affiliations of the CSE students. Two, geospatial analysis based on latitude and longitude of birth location. Three, network analysis of the CSE students based on all of their affiliations. In each of these three types of analyses it is possible to use techniques to elucidate underlying structure and begin to address historical similarities. Lastly, among many different types of analyses, one method used for all three approaches was to determine subgroups or clusters and to avoid confusion here the use of the term “cluster” as a lone descriptor will be restricted to HCA, while geospatial subgroups will be termed geospatial clusters, and network subgroups simply as network subgroups. Finally, throughout the article, key individuals will be integrated with several mini-biographical portraits to give more depth to the analysis. The conclusion will discuss how the CSE group demonstrated the importance of individual histories, group interrelationships, and the broader advance of Chinese political intellectuals who lived in the twentieth century.


# The Growth of Intellectual Activism among the Chinese Students Abroad


## Transformations in the 20th Century and the Role of Chinese Political Intellectuals


Living during rapidly changing historical times is a challenge for most individuals because they are so impacted by those changes. For the Chinese people after the Sino-Japanese War in 1894-95 the challenges were enhanced by a sense of urgency spurred by national humiliation. The early century Qing reforms, local community empowerment, downfall of the dynastic system in the 1911 Revolution, and subsequent warlord period, among other events, displaced many traditional values, ironically resulting in a cultural flourishing, particularly among youth born at the turn of the century. Young Chinese, especially among the upper classes and those who could afford education, searched for a way to save their nation, and pursue their own futures. Intellectuals were seen as key national leaders (<cite data-cite="626961/2MBY485A"></cite>). The modern ideas and societies of the West became a beacon for thousands of Chinese youths who committed themselves to intellectual activism and became what Shakhar Rahav has called political intellectuals. Rahav defines these people as:


*[K]nowledgeable, educated individuals who in a time of turmoil consciously tried to bear on the political and envision what they saw as a proper social order. These political intellectuals derived much of their identity and authority from the traditional status of the literati and school-officials in China as well as from their familiarity with new forms of (Western) knowledge, and from their access as consumers and producers to the media of the age—the printed word. . . . Intellectuals mediated between the public and contending visions of political legitimacy. . .* (<cite data-cite="626961/I9PRXQ7M"></cite>, p.4)


At a more granular level, Benjamin Elman elucidated the potentials of intellectual activism. He argued that in the difference between formal and applied knowledge, that “[m]ore than just autonomous individual choice is involved in cultural creation and transmission; social, political, and economic context do make a difference. As historians we need a new, constantly shifting, middle ground between historical functionalism and free will voluntarism, which will enable us to move back and forth more easily between the cultural forms of domination and individual or group forms of resistance.” (<cite data-cite="626961/3JJLCKI3"></cite>, p. 375). This multifaceted analysis is realized in the work of Timothy Cheek in his excellent work, *The Intellectual in Modern Chinese History*. Cheek’s comprehensive, insightful study of Chinese intellectuals literally maps out historical and ideological frameworks in which he discussed the shifting intellectual, cultural, and political roles of modern intellectuals. In the period of focus for this article Cheek contended that were several major defining questions that framed each epoch: “In 1905 it was how to save China. What kind of changes are needed to enable what is important in the world we grew up with to endure and prosper? In the 1920s the question of the day was how to awaken the Chinese people in order to save themselves from the clear and present danger of foreign domination and domestic misrule. By the 1940s it was how to build the New China. . . [Emphasis in original] (<cite data-cite="626961/NMJSICBH"></cite>, p. 321).


One could say that intellectuals throughout history have faced compelling reasons to seek their own *raison d'être* in personal and societal influences. This study is only a glimpse of a relatively small group of students to better illustrate the impacts of the influences and relationships surrounding them.


## Ambassadors to the West: Chinese Youth in Europe After WWI


In the case of the Chinese students who went to Europe there were many reasons to go abroad as Cai Yuanpei had exhorted, including their preconceptions of European intellectual and cultural trends and the educational options developed for them in the aftermath of World War I. Ruth Hayhoe in her comparative article on “The Cultural Dynamics of Sino-Western Educational Co-operation,” frames the different orientations between German, American, and French higher educational systems for the Chinese. Among the two European models, the Germans emphasized the applied sciences for modernization, even though the theoretical knowledge and professional training led to higher prestige. A second German approach was a blend of sciences and arts “with philosophy as a synthesizing discipline.” (<cite data-cite="626961/D7YWQNYV"></cite>, pp. 678–679). The French ideal was a focus on education in a grand mixture of disciplines for the modernization of the nation. The idea of the prestige of the intellectual as a public actor in the solidification of the state might have appealed to the Chinese. There are many statements on the affinities between the high cultures of China and France that support Hayhoe’s characterization of this mutual sense of common cultural orientations. For example, the following discerning observation was given by the Chief of the Chinese Labor Battalions, Louis Grillet, who in his closing report after World War I wrote in 1918:


*The Chinese culture is essentially philosophical, moral, and social, and if during the [last] five centuries, from the Ming until 1905, the mode of recruitment of the scholars has stressed a literary education that is detrimental to the thought [process], this has been contrary to the aspirations of the Chinese and designed to serve the defense of the dynasties. By the same token, the essence of French culture is also completely philosophical, moral, and social; the differences are in the development of science, industry, and literature.* (<cite data-cite="626961/23XGFHP4"></cite>, fol. AAE série E. Chine Vol 4 7).


Grillet’s characterization is interesting for the insightful framing even though it includes some stereotyping of Qing intellectuals.


Amidst the stimulating and often kaleidoscopic experiences of travel, study, and living abroad, the Chinese youth were thoughtful about their public responsibilities to their country. The notion of intellectuals as political intellectuals, as potential activists was heatedly debated among Chinese youth during the New Culture Movement, particularly among those who went to Europe. There was a plethora of opportunities for political activism rooted in youth groups developed in China and those also formed in Europe. Youth groups such as the Hunan-based New Citizen’s Study Society, the Tianjin-based Self-Awakening Society, and nationally based, Young China Association, generated international and local debates about China’s future, the potentials of Western political ideas, and the role of young people in that future.


Levine’s *The Found Generation*, chapter 5 - "The Chosen Path" follows four examples of Chinese who belonged to these youth groups and explores how this public discourse shaped their political transformations. One of the leaders of the Young China Association, Wang Guangqi (王光祈,1892-1936), who in many ways represented the intellectual soul of the Young China Association, eschewed adopting any political ideology for a vision of social reform. He earned a doctorate in music in Germany and wrote a thesis on Chinese opera. He published over 300 articles and dozens of books, and when he died of malnutrition his body was shipped back to China where three commemorations were given by distinguished Chinese scholars such as Fu Sinian (傅斯年, 1896-1950). In the mid-1980s Wang's role in promoting a national theory of Chinese music was recognized with a pavilion in Chengdu and a reissuing of his works on musical theory (<cite data-cite="626961/A2UXEAUZ"></cite>, Chapter 5).


Beginning in 1922, these public polemics on intellectual activism took place contemporaneously with the process of Chinese political party formations in Europe. There was direct communication between organizers in Europe and party organizers in China. A good example of this was the breadth of how the EGMD was formed in Europe during this period. The EGMD organizers were particularly successful at recruitment and generation of discourse among Chinese throughout France, Belgium, Germany, Holland, and had a special liaison with Chinese mariners. At the founding meeting of the EGMD, held in Lyon in November 1923, the speeches and actions were recorded in meticulous minutes. Quite clearly the recruitment of Chinese mariners, workers, and students was framed to promote the importance of Sun Yatsen’s principle of people’s livelihood. Wang Jingqi (王京歧,1895-1925) the EGMD organizer and first EGMD Chair, who had been expelled in the Lyon Incident in 1921, had returned to Europe to organize the EGMD under Sun Yatsen’s personal guidance, gave a strong speech in favour of the politically activist spirit expected by EGMD members. Another speaker at this meeting was Zhou Enlai (周恩來,1898-1976) who critiqued May Fourth activists who lingered in the discussions and not the praxis of revolutionary action. Zhou argued that following an ideology did not mean a subordination of oneself, but a liberation of the self, and an empowerment of the necessary political will to act (<cite data-cite="626961/CL4AYSZY"></cite>, pp. 53–60).


The EGMD had greater numbers than the ECCO in Europe, but the ideological orientation was more leftist, and in reality, the United Front was controlled by the Communists. A key EGMD founder, who was a conservative, Fang Ditang (方棣棠,1899-1968) was in the CSE group from UTC. In fact, Fang was the key founding leader of the Belgium section for the EGMD and elected Vice-Chair after Wang Jingqi as Chair. In 1925 Fang was expelled from the EGMD along with fifteen others at a meeting chaired by Deng Xiaoping (鄧小平, 1904-1997) (*discussed in detail below*) (<cite data-cite="626961/CL4AYSZY"></cite>, pp. 90–101).


This first section has briefly introduced the concept of the academic politicians, who were intellectual activists. The CSE group included students who became academic politicians and some who abandoned their studies for revolutionary careers. The remainder of the article will focus on the CSE group to understand group and individual dynamics through an integrative approach.

<!-- #region tags=["hermeneutics"] -->
The idea of a more integrative approach – utilization of wider perspectives was suggested by Tsou Tang in his seminal work, “Interpreting the Revolution in China: Macrohistory and Micromechanisms.” Tsou remarked: “The general proposition is the following: the Chinese case shows that the processes of innovation, systematization, and strategic interaction in the choices made by the political actors are direct and readily observable micromechanisms leading to macrohistorical changes, particularly the transformation of one political system into another one.” (<cite data-cite="626961/38E5R87A"></cite>, p. 228). By utilizing narrative on the wide and small scale, quantitative and network analyses, it is contended that an enriched prosopography approach illuminates the environmental, social, and political choices of those students who became political intellectuals and those who chose to become revolutionaries.
<!-- #endregion -->

# A Multivariate Analysis of the CSE


## A Profile of the CSE Group


After briefly introducing the political intellectuals in the European study abroad during the interwar years, this section will statistically analyse the specific dataset of the CSE group who attended specific institutions in terms of selected attributes, birth and death years, geospatial origins, and similarities of attributes as expressed in hierarchical clustering.

<!-- #region tags=["hermeneutics", "narrative"] -->
[Table 2](#anchor-table-2) displays several attributes that demonstrate selected institutional affiliations, provincial origins, academic professions, and political affiliations. These give an overall view that will be further discussed in the graphs and tables in the statistical and network analysis. Here it will be remarked that the 16 women represent 8 percent of the CSE group, which was slightly higher than the CBD as a whole, where women represented only 7 percent of the total. It is clear that the EGMD was by far the most active political party among the Chinese in Europe. They were under the direction of the GMD Overseas Bureau and had a dynamic recruitment success internationally. The GMD also was the most formidable party in China at the time.
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 2: Number of Individuals for selected affiliations CSE group (N=197). *Of known factional affiliation for EGMD there were 27 leftists, 9 rightists and 16 Communist individuals."], "type": "table"}} tags=["table-2", "hermeneutics", "anchor-table-2"] -->
| **Attributes**            | **Number** |
|---------------------------|------------|
|     IFCL                  |     90     |
|     Academic Careers      |     74     |
|     EGMD*                 |     71     |
|     UTC                   |     66     |
|     Guangdong             |     47     |
|     ECCO                  |     37     |
|     Scientists            |     34     |
|     Hunan                 |     32     |
|     Sichuan               |     28     |
|     UP                    |     20     |
|     Jiangsu               |     19     |
|     UB                    |     17     |
|     Female                |     16     |
|     Arts & Letters        |     16     |
|     Social Scientists     |     14     |
|     Academic Education    |     10     |
|     Political Leader      |     8      |
|     SDP                   |     8      |
|     GYS                   |     7      |
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
## Analysis of Birth Year and Death Year
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
Birth year generational cohort can often result in substantive and long-lasting formative development in the lives of individuals as noted by sociologists, psychologists, and historians. The mean birth year for the CSE group was the year 1899 with the youngest year being 1877 and the oldest year being 1914. As displayed in figure 1 there is fairly tight clustering of birth from 1892 through 1906 (68% of all students). When these youth decided to go to Europe, they already were near or in their second decade of life, with relationships and establishing their ideas of politics and developing adult social norms. The Chinese born during this time period directly experienced the impact of abolishing an examination, the introduction of Western-style schooling, and the development of youth groups and activism during the New Culture Movement. These social and political events added to this generation’s cohesion, identity, and sense of mutual purpose as they travelled to Europe. Thus, how important was the European experience in terms of influencing their relationships, careers, and ideas?
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 1: Distribution of birth year for the CSE group (N=143). There are 54 missing birth years."], "type": "image"}} tags=["figure-1", "hermeneutics"]
library("IRdisplay")
display_png(file="./media/Fig1.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
The mean death year for the CSE group was 1976 (±20.0). As displayed in figure 2 there is a high grouping of deaths from about 1956 through 1996. What is most intriguing about this group is that only18% of the 83 individuals whose death dates are known, died during the tumultuous half a century all through key political conflicts after the dissolution of the first United Front in 1927 through the second Sino-Japanese War and beyond to the anti-intellectual campaigns after the establishment of the PRC. Even for the 37 members of the ECCO, their death year averages dramatically contrasted with the comrades who also went to the Soviet Union, a cohort of 55 individuals who lost 30% of their membership from 1925-1931.  Although some of the CSE group did go to the Soviet Union, only 2 people died in the 1920s and 1 person died in the 1930s, a stark contrast to 18 Euro-Soviet members who died between 1924 and 1930 (<cite data-cite="626961/PT8ARAUT"></cite>). However, until the data in the CSE group is expanded on death year, the results are only initial suggestive of death rates versus political involvements, especially as the degree of involvement is not reported here.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 2: Distribution of death year for the CSE group (N=83). There are 114 missing death years."], "type": "image"}} tags=["figure-2", "hermeneutics"]
library("IRdisplay")
display_png(file="./media/Fig2.png")
```

## Analysis of Birthplace-Province and City


Regional influence on individual identity and group formations is well-known in historical studies. This study also showed that provincial origin has some impact in the multivariate, geospatial, and network analyses. This section will explore in-depth provincial data.

<!-- #region tags=["hermeneutics", "narrative"] -->
In addition to the general provincial participation, the pattern of student provincial origin and educational selection is interesting to observe as seen in [table 3](#anchor-table-3). Of the 184 students who attended the four selected institutions, who have known birth data, Guangdong, Hunan, and Sichuan students comprised 58% of the students (N=52) of the IFCL and 68% of the students at the UTC (N=42) for the CSE group. On the other hand, these three provinces represented a smaller percentage of students at UP (N=5) at 28 percent, and UB (N=5) at 30 percent.
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 3: Birth provinces of CSE number of individuals, 1900 provincial populations, and ratio of province population to number of participants."], "type": "table"}} tags=["table-3", "hermeneutics", "anchor-table-3"] -->

| Province       | Number of Individuals | 1900 Population | % of All China | Area (km²) | Density / Km | Individual per Million | Individual per Km |
|----------------|-----------------------|-----------------|----------------|------------|--------------|-----------------------|-------------------|
| Anhui          | 6                     | 23,670,300      | 5.9            | 139,900    | 169          | 3.95                  | 28.20             |
| Fujian         | 6                     | 12,876,500      | 3.2            | 123,100    | 105          | 2.15                  | 17.43             |
| Guangdong      | 47                    | 31,865,300      | 7.9            | 366,500    | 87           | 0.682                 | 1.85              |
| Guangxi        | 4                     | 5,142,300       | 1.3            | 220,400    | 23           | 1.29                  | 5.83              |
| Guizhou        | 3                     | 8,703,000       | 2.2            | 174,000    | 50           | 2.90                  | 16.67             |
| Hainan3        | 4                     | 219,500         | 0.22           | 34,300     | 6            | 0.052                 | 1.60              |
| Hebei          | 14                    | 35,280,700      | 8.8            | 202,700    | 174          | 2.52                  | 12.43             |
| Heilongjiang   | 0                     | 2,029,000       | 0.5            | 463,600    | 4            |                       |                   |
| Henan          | 9                     | 35,316,800      | 8.8            | 167,000    | 211          | 3.92                  | 23.50             |
| Hubei          | 2                     | 35,280,700      | 8.8            | 187,500    | 188          | 17.64                 | 94.08             |
| Hunan          | 32                    | 22,169,700      | 5.5            | 210,500    | 105          | 0.692                 | 3.29              |
| Inner Mongolia | 0                     | 604,000         | 0.2            | 1,177,500  | 0.51         |                       |                   |
| Jiangsu        | 19                    | 13,980,200      | 3.5            | 102,600    | 136          | 0.742                 | 7.17              |
| Jiangxi        | 4                     | 26,532,100      | 6.6            | 164,800    | 161          | 6.63                  | 40.25             |
| Liaoning       | 1                     | 9,000,000       | 2.2            | 151,000    | 60           | 9.00                  | 59.60             |
| Shandong       | 1                     | 38,247,900      | 9.6            | 153,300    | 251          | 38.43                 | 250.67            |
| Shanxi         | 0                     | 12,200,500      | 3.0            | 157,100    | 78           |                       |                   |
| Shaanxi        | 1                     | 8,450,200       | 2.1            | 195,800    | 43           | 8.45                  | 43.16             |
| Sichuan        | 28                    | 68,724,900      | 17.1           | 569,000    | 121          | 2.45                  | 4.31              |
| Zhejiang       | 9                     | 11,580,700      | 2.9            | 101,800    | 114          | 1.29                  | 12.64             |
| Mean       | 11.2              | 20,102,715  |                | 253,120| 104      | 6.05              | 36.63         |
| **Total**      | **190**               | **402,054,300** |                | **5,062,409**|            |                       |                   |
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
*Notes: Population for 1900 [source](http://populstat.info/Asia/chinap.htm), Hainan is separately calculated (see title above). Ratios less than 1, e.g., 0.68 is one individual per 677,895. There are seven individuals missing province data. Hainan population statistics are obtained from doctoral thesis of Zhou Wenpei based on 1935 data (<cite data-cite="626961/BYJQVKQM"></cite>).*
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
Numerical participation, compared with population, did show a general correlation, regression analysis had an R<sup>2</sup> of 0.2342 and a p-value of 0.031 was insufficient due to outliers and some with great leverage. There were several provinces that were far out of the 68% confidence limit, i.e., Guangdong, Hunan, Jiangsu, and Shandong making any conclusion that participation followed with larger provincial population was unacceptable, which is not surprising since emigration or temporary emigration to Europe was probably not due a single causal factor. Density as a predictor was worse than population, R<sup>2</sup>=0.0164 and p=0.592.
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 4: Provincial origin and educational attendance (N=187) for the CSE group and some political affiliation data. There are seven individuals missing province data."], "type": "table"}} tags=["table-4", "hermeneutics", "anchor-table-4"] -->
| Province  | Count | Percent | UTC | SFI | UBerlin | UParis | ECCO | EGMD | EGMDLeft | EGMDRight |
|-----------|-------|---------|-----|-----|---------|--------|------|------|----------|-----------|
| Anhui     | 6     | 3.2%    | 0   | 4   | 1       | 1      | 2    | 2    | 0        | 0         |
| Fujian    | 6     | 3.2%    | 2   | 4   | 0       | 0      | 0    | 2    | 0        | 0         |
| Guangdong | 47    | 24.7%   | 17  | 29  | 0       | 2      | 5    | 20   | 7        | 3         |
| Guangxi   | 4     | 2.1%    | 1   | 2   | 0       | 1      | 2    | 2    | 0        | 0         |
| Guizhou   | 3     | 1.6%    | 2   | 1   | 0       | 0      | 1    | 2    | 0        | 0         |
| Hainan    | 4     | 2.1%    | 0   | 3   | 0       | 1      | 0    | 2    | 1        | 0         |
| Hebei     | 14    | 7.4%    | 3   | 7   | 1       | 2      | 5    | 3    | 0        | 1         |
| Henan     | 9     | 4.7%    | 4   | 3   | 1       | 1      | 1    | 2    | 1        | 0         |
| Hubei     | 2     | 1.1%    | 1   | 1   | 0       | 0      | 0    | 0    | 0        | 0         |
| Hunan     | 32    | 16.8%   | 9   | 17  | 3       | 2      | 6    | 12   | 5        | 0         |
| Jiangsu   | 19    | 10.0%   | 4   | 8   | 5       | 2      | 2    | 6    | 4        | 1         |
| Jiangxi   | 4     | 2.1%    | 0   | 2   | 1       | 1      | 0    | 2    | 3        | 0         |
| Liaoning  | 1     | 0.5%    | 0   | 0   | 0       | 1      | 0    | 0    | 0        | 0         |
| Shaanxi   | 1     | 0.5%    | 0   | 0   | 1       | 0      | 1    | 0    | 0        | 0         |
| Shandong  | 1     | 0.5%    | 0   | 1   | 0       | 0      | 0    | 1    | 0        | 1         |
| Sichuan   | 28    | 14.7%   | 17  | 6   | 2       | 2      | 8    | 9    | 2        | 1         |
| Zhejiang  | 9     | 4.7%    | 3   | 2   | 1       | 3      | 0    | 2    | 1        | 1         |
| **TOTAL** | **190** | **100.0%** | **63** | **90** | **16** | **19** | **33** | **67** | **24** | **8** |
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
In [Table 4](#anchor-table-4), there appears to be interesting representation by province and institutional affiliation in the data. Among the students attending the four selected institutions, 95% (N=187) had known birth province, while three provinces, Guangdong, Hunan, and Sichuan, the largest contributions comprised 58% (N=52) of the IFCL attendees with 68% (N=43) of the students at the UTC. On the other hand, these three provinces represented a smaller percentage of students at 28% (N=5), and UB at 30% (N=5). In addition to university attendance by province, [Table 4](#anchor-table-4) also has a summary of the average provincial counts, and affiliation by the ECCO, the EGMD, the leftist-EGMD, and the rightist-EGMD.
<!-- #endregion -->

An even stronger provincial origin emerges when one creates historical maps that pinpoint the birth geospatial location and its inevitable impact on an individual for years and uses that as a comparison to other historical factors under investigation. This was done for all participants with known birth locations 73% (N=144) of all CSE. Besides reporting distributions here in several figures one interesting computation was done to simply determine the shortest physical distance (Km) to each closest neighbour which is seen in [Table 5](#anchor-table-5) for Guangdong (N=26), Hunan (N=30), and Sichuan (N=28).  In Guangdong there are several individuals who are separated by zero distance due to being from the same city, while in Hunan 42% (N=11 out of N=26) are from the same city (Changsha) and in Sichuan only 23% (N=5) are from the same city (Jiangjin) but several others are close but not in the same city. Guangdong also has a further eight individuals who are thirty or less kilometres apart or a day’s walk away.

<!-- #region jdh={"object": {"source": ["table 5: Distances in the Nearest Neighbor in Three Provinces."], "type": "table"}} tags=["table-5", "hermeneutics", "anchor-table-5"] -->
| **Guangdong (N=26) (2)** |                   |     | **Hunan (N=30) (2)** |                   |     | **Sichuan (N=28) (2)** |                   |     |
|:------------------------:|:-----------------:|:---:|:--------------------:|:-----------------:|:---:|:----------------------:|-------------------|-----|
| Chen Chuanyong           | He Chichang       | 0   | Cao Dumou            | Chen Jie_1        | 0   | Feng Xuezong           | Zuo Shaoxian      | 0   |
| Yang Qian                | Zhang Wenjia      | 0   | Chen Yinke           | Chen Shunong      | 0   | Guo Qingzheng          | Luo Jingzhong     | 0   |
| Yuan Zhenying            | Chen Chuanyong    | 0   | Fan Xinqun           | Chen Shunong      | 0   | Jian Lian              | Li Huang          | 0   |
| Yuan Zhuoying            | Chen Chuanyong    | 0   | Fan Xinshun          | Chen Shunong      | 0   | Jiang Zemin_1          | Kuang Hongru      | 0   |
| Zhai Junqian             | Chen Chuanyong    | 0   | Hu Zaiyu             | Peng Xiang        | 0   | Kuang Hongru           | Jiang Zemin_1     | 0   |
| Liang Tianyong           | Ou Shengbai       | 2   | Li Dan               | Chen Shunong      | 0   | Li Huang               | Jian Lian         | 0   |
| Chen Guoliang            | Xu Shuping        | 8   | Shu Zhirui           | Chen Shunong      | 0   | Luo Jingzhong          | Guo Qingzheng     | 0   |
| Fu Chuanbo               | Xu Shuping        | 12  | Wei Bi               | Chen Shunong      | 0   | Nie Rongzhen           | Jiang Zemin_1     | 0   |
| Fang Ditang              | Xu Shuping        | 22  | Xu Teli              | Chen Shunong      | 0   | Shi Limu               | Jiang Zemin_1     | 0   |
| Cui Zaiyang              | Chen Chuanyong    | 25  | Yang Chao            | Chen Shunong      | 0   | Xie Zeyuan             | Guo Qingzheng     | 0   |
| He Yanxuan               | Ou Shengbai       | 26  | Yang Gengtao         | Chen Shunong      | 0   | Zhang Xi               | Jiang Zemin_1     | 0   |
| Zheng Yanfen             | Liang Tianyong    | 27  | Yang Runyu           | Chen Shunong      | 0   | Zuo Shaoxian           | Feng Xuezong      | 0   |
| Yang Yixiang             | Fu Chuanbo        | 29  | Zhu Zhenwu           | Chen Shunong      | 0   | He Luzhi               | Jian Lian         | 14  |
| Liu Shixin               | Zheng Yanfen      | 30  | Zhou Dunxian         | Chen Shunong      | 39  | Zhou Yongsheng         | Jiang Zemin_1     | 34  |
| Zhang Lianjie            | Chen Guoliang     | 32  | Ouyang Tai           | Hu Zaiyu          | 58  | Chen Chongxian         | Gan Rui (8)       | 49  |
| Zhang Yun                | He Yanxuan        | 56  | Li Shengyi           | Zhou Dunxian      | 60  | Liu Bojian             | Chen Jiesheng (7) | 88  |
| Yan Jijin                | Long Zhanxing (3) | 64  | Liu Mingyan          | Yang Zifu         | 66  | Shen Shilin            | Chen Chongxian    | 94  |
| He Chaodong              | Yang Yixiang      | 71  | Yang Zifu            | Liu Mingyan       | 66  | Wang Yaoqun            | Guo Qingzheng     | 121 |
| Zhang Guiyuan            | Cao Xisan (4)     | 72  | He Changgong         | Li Shengyi        | 70  | Wang Bingnan  (7)      | Liu Bojian        | 305 |
| Li Tingyin               | Zhu Xi (5)        | 86  | Cao Xisan            | Zhang Guiyuan (6) | 72  |                        |                   |     |
| Yan Jijin                | Chen Shoumin (3)  | 93  | Xiao Zhensheng       | Cao Xisan         | 82  |                        |                   |     |
| Liang Shanjin            | Zhang Guiyuan     | 97  | Xie Qing             | Cao Dumou         | 84  |                        |                   |     |
| Lai Guogao               | Zhang Guiyuan     | 103 | Peng Shiqin          | Ouyang Tai        | 87  |                        |                   |     |
| Yan Jijin                | Huang Shitao (3)  | 214 | Li Jingan            | He Changgong      | 116 |                        |                   |     |
|                          |                   |     | Chen Cong            | Yang Zifu         | 138 |                        |                   |     |
<!-- #endregion -->

*Note: Distances (km, decimals rounded up) to the Nearest Neighbor in Three Provinces, obtained via ArcGIS Pro 3.3 and the Generate Near Table tool. (2) Number of individuals measured. Individuals from (3) Guangxi, (4) Hunan, (5) Zhejiang, (6) Guangdong, (7) Shaanxi, (8) Sichuan.*

<!-- #region tags=["hermeneutics", "narrative"] -->
In looking at institutional affiliations, politics, and careers of these individuals, it is clear that their regional orientations, as represented in the nearest neighbour table resulted in situations where on the one hand, they carried forward their regional friendships, but on balance there were new alliances and allegiances cultivated in Europe. For example, if one assesses the first nine rows in the Guangdong column of nearest neighbours up to a distance of 12 kilometres – there are twelve individuals. All twelve were within easy walking distance from each other and with only one exception, all going to educational institutions during 1921. Nine of these individuals went to the IFCL, two to Charleroi, and one individual is unknown.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
Of the intellectual work, there were five individuals who completed a thesis, including the one female, Liang Tianyong (梁天咏, b.1901), who attended the IFCL and then received her diplomas in French and pedagogy at the University of Dijon and the University of Lyon respectively. She received her doctorate of letters in 1931 with a thesis about masculine and feminine education according to Jean-Jacques Rousseau.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
Given the smallness of the 12 individual sample it is interesting that there were five EGMD members split into two known-leftist orientations, two known-rightist orientation and one unknown. It is intriguing, but not perhaps surprising, that relatively close neighbours growing up in China evolve in such different ways in Europe. There also were two ECCO members, at least one Anarchist member, and one SDP member. The elder of two brothers, Yuan Zhenying (袁振英,1894-1979), who had been a Communist in China, abandoned the party after he came to France. Yuan returned to China at the request of Zou Lu  (邹鲁,1884-1954), rector of Sun Yatsen University, to help him with educational issues at Sun Yatsen University, while his younger brother, Yuan Zhuoying (袁擢英, b.1898) stayed on at the IFCL and became an EGMD-leftist. In his thesis, Shiu Wentang lists both brothers as having Anarchist affiliations (<cite data-cite="626961/EEUJZFU3"></cite>).  Same city and same family did not necessarily mean a same outcome to the European venture.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
Following are five maps that give geospatial locations of the CSE Chinese in China from the country level down to intra-provincial maps with individual names. [Figure 3](#anchor-figure-3) shows the birth origin within provincial boundaries and the country-wide distribution of this sample of 144 CSE individuals (53 individuals did not have known city origins).
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 3: CSE birth cities (N=144). There are 53 missing birth cities. Administrative boundaries 1911-1921 from Henriot, 2021."], "type": "image"}} tags=["hermeneutics", "figure-3", "narrative", "anchor-figure-3"]
library("IRdisplay")
display_png(file="./media/Fig3.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
When looking at this country-wide map (<cite data-cite="626961/BW5IFKB3"></cite>) it is apparent that not all provinces sent students or sent them in the same number.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 4: Country-wide distribution with concentrations of geospatial clusters for CSE group at this scale.  (N=144). There are 53 missing birth cities."], "type": "image"}} tags=["hermeneutics", "narrative", "figure-4", "anchor-figure-4"]
library("IRdisplay")
display_png(file="./media/Fig4.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
[Figure 4](#anchor-figure-4), at a smaller scale, shows geospatial clusters at specific locations: e.g., around Changsha, Hunan or around Chongqing in Sichuan. Intra-province distributions showed distinct clusters, with the largest being in Hunan, which had a significant cluster around Changsha.
<!-- #endregion -->

At a smaller scale, figures 5-7 show birth locations in Guangdong, Hunan, and Sichuan. While Guangdong participation is located in two clusters along the coast; Hunan participants are primarily located along the Xiang River area. Sichuan CSE participants are located in the two key areas of Chongqing and Chengdu.

```R jdh={"object": {"source": ["figure 5: CSE birth cities for Guangdong CSE group (N=30). Four Hainan individuals are included as part of Guangdong during this period. Occluded individuals are listed in the text."], "type": "image"}} tags=["hermeneutics", "narrative", "figure-5"]
library("IRdisplay")
display_png(file="./media/Fig5.png")
```

```R jdh={"object": {"source": ["figure 6: Birth cities for Hunan CSE group (N=28). Occluded individuals are listed in the text."], "type": "image"}} tags=["hermeneutics", "narrative", "figure-6"]
library("IRdisplay")
display_png(file="./media/Fig6.png")
```

```R jdh={"object": {"source": ["figure 7: Birth cities for Sichuan CSE group (N=22). One occluded individual is listed in the text."], "type": "image"}} tags=["hermeneutics", "narrative", "figure-7"]
library("IRdisplay")
display_png(file="./media/Fig7.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
There are some occluded individuals in figures 5-7 that are due to closely spaced labels as well as duplicate birth city coordinates. The occluded individuals include In the Guangdong/Dongguang - Guangzhou cluster: Yuan Zhenying, Yuan Zhuoying, and Zhai Junqian; in the other Guangdong clusters Li Tingyin, Liang Tianyong, Yan Jijin, and Zhang Wenjia; In the Hunan Changsha cluster: Li Dan, Xu Teli, Yang Chao, Yang Gengtao, Yang Runyu, and Zhu Zhenwu; and in the Sichuan province group: Zhou Yongsheng.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
The geospatial figures 5-7 show the origin locations for these students. The support and activities at the provincial level could impact their educational choices. As an example, the influence of Guangdong is embedded in the founding history of the IFCL. The first students were set to begin by the end of 1921. Although worker-students already in France (largely from Sichuan and Hunan) thought that they would be assigned these places, in fact, whether for politics or personal reasons, Wu Zhihui recruited under his patronage and a new set of students were recruited from around China. Cantonese students were recruited in a large group through the offices of Zou Lu, whose institution was willing to fund the students. In Belgium, the UTC administration also was encouraged to recruit by the same educators, especially under the educational leadership of Li Shizeng. Thus, it is unsurprising that one finds more than one quarter of the UTC students are from Guangdong, several of whom were to join the rightist faction of the EGMD. It is significant that there only were two individuals from Guangdong in this data who attended the UP or the UB. The IFCL and Guangdong relationship is articulated in an article by Lan Shude and Huang Yu. Seventy-eight students from Guangdong comprised government-funded students out of the first 138 students in 1921 and 165 out of 473 students in total. This could be explained in terms of the nature and funding of the IFCL. IFCL was established as the overseas department of several Chinese universities including mainly Beijing Sino-French University and Guangdong University. Money that was meant to fund the Southwest University, which then failed to be created due to Guangdong’s political turmoil, was partly given to IFCL under the direct official order of Sun Yatsen, the President of the Guangdong government in 1925. Between 1921 to 1926 before the Boxer indemnity had actually been paid, the IFCL was funded mainly by the Guangdong, Beijing, and French governments. Lan and Huang also found that 37 Cantonese ICFL student obtained their doctoral degrees in France, while quite a few of them returned to become professors at Sun Yatsen University. For a detailed list of the Cantonese students’ profiles and the introduction of outstanding Cantonese ICFL students who became prominent figures in modern China see the article on the IFCL by Lan and Huang (<cite data-cite="626961/VHPCKZYS"></cite>).
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
In addition to the Guangdong students, there was a group of Sichuanese (N=16), and Hunanese (N=8) who were work-study students who also attended UTC, because it was a worker’s university, and the Belgians were thought to be warmer in their treatment of Chinese. Jiang Zemin (江澤民,1903-1989) who was from Jiangjin, Sichuan and was the roommate of Nie Rongzhen (聶榮臻,1899-1992), related in a 1985 interview how important this birth city connection was in terms of Nie, who encouraged him and others to attend UTC. Jiang and Nie had gone to the same school back home, although Nie was older by three years. Still the city connection meant a great deal. At UTC they roomed together, and Jiang Zemin became an ardent revolutionary, but he also graduated with a degree in engineering (Xi Li, personal communication, October 25, 1985) (<cite data-cite="626961/EYP3RMGJ"></cite>). In fact, within the CSE group there were five other individuals from Jiangjin, Sichuan. With regard to birth city and individual choices, the larger CBD included eighteen Chinese from Jiangjin, Sichuan and many of them followed Nie Rongzhen to the Soviet Union and back to China to fight in the revolution.  Several Jiangjin individuals died in the Nanchang Uprising and the battle of Honghu. Clearly, place mattered to these Chinese, especially as they gathered in a foreign country. Yet, many individuals also opened up to broader regional potentials for their political affiliations. This trend especially was true for the EGMD and the ECCO when one examines the array of regional affiliation and official representations and party activities.
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
## Cluster Analysis of the CSE group
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
Hierarchical cluster analysis (HCA) is a multivariate statistical analysis that determines similarities via distance and in this case, it was Euclidean distance. The clustering algorithm was the more stringent or conservative Ward linkage method (<cite data-cite="626961/S8SYJ28F"></cite>) The production of the resulting hierarchy is expressed in a dendrogram (also known as a tree diagram) that graphically displays distances based on similarities between these studied entities. The shorter the connecting linkage line between individuals, the higher the similarity. Conversely, distantly related individuals are further apart and link at much higher levels. Thus, all similar individuals in the dendrogram are grouped into clusters that express their similarities in two ways. First, each individual is proximate to their nearest neighbor, with a linkage showing the connection or linkage level. Secondly, gaps can be seen between clusters or some single individuals that helps to identify cohesive clusters.
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
There are numerous analytical frameworks that use different algorithms. For a discussion of hierarchical clustering see the article *Revolutionary Roads*, that is included in a collection of digital Chinese history that explores elites and power (<cite data-cite="626961/PT8ARAUT"></cite>). To assist cluster identifications, one can use statistical methods to determine number of clusters via “validity indices” that can be used as recommended starting points and then a researcher can make slight adjustments to the final number of dendrogram clusters based on the historical record and knowledge of each cluster member. Five validity indices were used in this study, i.e., root-mean square standard deviation (RMSSTD), pseudo F-ratio (CHF), pseudo T-square statistic (PTS), Davies-Bouldin’s index (DB), and Dunn’s cluster separation measure (DUNN).These indices simply use different methods to quantitate the variance or variability among the distances to identify slow or fast changes with neighbors and hence cluster presence/absence (<cite data-cite="626961/N94EW2PA"></cite>).
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
Why HCA is useful for historians is that the analysis is based on all the available affiliations, rather than focusing on one or two affiliations, i.e., it is a multivariate method rather than a univariate method. For example, oftentimes the use of only one or two commonly held political positions, common group affiliations, or similar career types are considered in historical narratives. What the HCA analysis can accomplish is to expand the factual foundation and discern patterns that cannot necessarily be determined by only one or two political positions as mentioned above. Numerous types of affiliations such as positions or group memberships that can all be analyzed in a more holistic way. The importance of both cluster analysis and network subgroup analysis as a lens to investigate groups of individuals allow one to discern new findings that are in the data. High data numbers maximize reliability, elucidate factors that were either unknown or ignored, and are easily handled by quantitative and network approaches that also allow multiple iterations of the data in different forms. This larger number of affiliations capacity can help scholars overcome a priori assumptions and substantiate a more reliable view of probable relationships and commonly lead to new research directions.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 8: Hierarchical cluster analysis of CSE individuals (N=197, affiliations=205)."], "type": "image"}} tags=["hermeneutics", "narrative", "figure-8", "anchor-figure-8"]
library("IRdisplay")
display_png(file="./media/Fig8.png")
```

<!-- #region tags=["hermeneutics"] -->
[Figure 8](#anchor-figure-8) is a dendrogram from the cluster analysis of the CSE group (N=197, 205 affiliations) showing fifteen cluster groups, names listed in [Table 6](#anchor-table-6). Chinese names with Chinese characters are displayed in [Table 12](#anchor-table-12).  Selecting the vertical height line at different percent determines the number of clusters to the right but has no effect on linkages between individuals. The dendrogram height line was set a 41.5% which yielded 15 clusters that was chosen due to three factors: the pronounced gaps between the clusters; the cluster memberships that followed the historical record; and statistical validity indices indicating how many clusters were likely present.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
The following are descriptions and characteristics for each of these fifteen clusters in figure 8.
* Cluster three (N=8) is uniquely all women. They represent half the women in the CSE dataset. They are geographically diverse, and they were more purposeful about obtaining their degrees, with half at the IFCL, one at Lyons University and Montargis College and three attended the University of Paris. Most of these women had academic related careers and were involved in GMD politics and some in the Democratic Movements. Two individuals, Fan Xinqun (範新群, n.d.) and Fan Xinshun (範新順,1896-1981), were cousins at the IFCL who married two other students at the IFCL, Peng Xiang (彭襄1897-1985) and Yang Chao (楊超,1899-n.d.) respectively. According to their studies, Luo Jiaying, 羅嘉穎 and Huang Yu黄峪,  illuminate romances and marriages that occurred at the IFCL, and some of the IFCL females married men who were accomplished academics at other Western institutions, such as renowned writer Su Xuelin, (蘇雪林, 1897-1999) (<cite data-cite="626961/UXHTQAAX"></cite>, <cite data-cite="626961/23FF6SWQ"></cite>).
* Clusters four through six (N=69) are all IFCL students, with divisions largely based on politics and province. In cluster four (N=27) with one exception, twenty-six individuals are EGMD, nine individuals are from Guangdong and there are eight scientists. Cluster five (N=17) has ten individuals from Hunan (half of whom are from Changsha), only four members in the EGMD, four in the ECCO, and one SDP member. Cluster six (N=25) has almost half of the individuals from Guangdong (N=12). This is the most politically diverse of these three IFCL clusters. Six members are EGMD, six SDP members, six GYS members, and one QND member, Lai Guogao ( 賴國高, b.1908-n.d.).
* Clusters seven through ten (N=63) includes all but two members affiliated with UTC. The two members who matriculated at the UP, He Luzhi (何魯之,1891-1978) and Li Huang (李璜,1895-1991) were ardent founders of the QND. While Guangdong was the largest regional grouping (N=16) in cluster seven (N=39), Sichuan was its largest regional grouping in cluster nine (N=16). Cluster eight (N=4) has four high-ranking ECCO members, three of whom joined the EGMD as well, while the much larger cluster seven has nine ECCO members and only two EGMD members. This is indicative of the sparser data available at present for UTC, which needs further research discoveries. Cluster ten is uniquely one individual, Nie Rongzhen, who as we will see below is the most central individual in the network analysis.
* Clusters eleven through fifteen (N=35) have three prestigious academics who are in cluster eleven and all attended the UB and includes the distinguished Chinese historian, Chen Yinke, who was mentioned in the introduction. These clusters include sixteen individuals who attended the UB and eleven who matriculated at the UP. As mentioned earlier, Guangdong has only one individual in these clusters, while Sichuan is represented by five people, and Hunan with five individuals. These clusters included distinguished Chinese academics in the sciences, particularly physics, and the arts and humanities. Among the most famous couples in the CSE were physicists, Qian Sanqiang (錢三強, 1913-1992) and He Zihui (何澤慧,1914-2011). Carsun Chang (張君勱, 1887-1969) who founded a third party, and intellectuals such as Xu Deheng (許德珩,1890-1990) who formed National Salvation groups, are in these clusters. Many of these individuals like Zhang Bojun (章伯鈞, 1895-1969) were later victims in the Great Proletarian Cultural Revolution (GPCR) for their support of democratic movements. Qian Sanqiang was a renowned scientist who studied nuclear physics in France after graduating from Tsinghua University. Working with his wife, He Zehui, who was also a nuclear physicist, they won the 1946 Physics Prize of the French Academy of Sciences for discovering a new fission technique. After returning to the mainland Qian became an academic leader and a member of numerous world delegations. In 1957 He Zehui won an award for her paper, "Research into the Process of Preparing Nuclear Emulsoid." Both were purged during the GPCR but later restored to their work.
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 6: Hierarchical cluster of membership CSE individuals (N=197, Affiliations=205). Individuals listed by cluster number from figure 8."], "type": "table"}} tags=["table-6", "hermeneutics", "anchor-table-6"] -->

| Cluster | Individuals                                                                                                                                                                                                                       |     |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| C1      | Long Zhanxing, Yan Jijin, Yang Qian, He Chichang, Fang Ditang, Zhang Wenjia, Qiu Zhengou, Yuan Zhuoying, Wu Wenan, Zheng Yanfen                                                                                                   |     |
| C2      | Yang Kun, Zhang Ruoming, Liu Mingyan, Xie Qing, Peng Xiang, Zhou Chonggao, Zhang Bojun, Peng Shiqin, Zhu Zhenwu, Li Pingheng, Fan Ying, Liu Puqing                                                                                |     |
| C3      | Wei Bi, Fan Xinqun, Fan Xinshun, Wu Mengban, Shu Zhirui, Yuan Jianqin, Li Hao, Liang Tianyong                                                                                                                                     |     |
| C4      | Han Luchen, Cai Shichun, He Jingqu, Li Shixiong, Liu Keping, Liu Wu, Zhao Yangxuan, Li Qijue, Lu Xiafei, Zeng Boliang, Wang Shumei, Hou Jinxiang, Liu Chong, Zhang Ruijiu, Huo Jinming, Xu Dahong, He Zhaoqing, Zhou Song, Di Fuding, Ye Yunli, Cheng Hongshou, Li Lianggong, Wang Deyao, Zeng Yi, Tang Xueyong, Liu Wentao, Shang Wu |     |
| C5      | Yang Runyu, Cao Xisan, Chen Shunong, Yang Chao, Zhang Nong, Li Dan, Xiao Zhensheng, Yang Gengtao, Yang Jie, Yao Baozhi, Jin Shuzhang, Zheng Dazhang, Ma Guangchen, Zhang Tong, Shu Hong, Fu Lun, Ouyang Tai                       |     |
| C6      | Hua Lin, Cui Zaiyang, Huang Ye, Ou Shengbai, Liu Shixin, Yuan Zhenying, Huang Xuan, He Yanxuan, Zhang Yun, Zhang Wuyuan, Li Guocai, Zhai Junqian, Chen Shaoyuan, Lai Guogao, Long Yin, Zhou Faqi, Zhu Yancheng, Fan Huiguo, Fu Chuanbo, Zhang Delu, Cao Qingtai, Zhao Yanlai, Zheng Shiyan, Deng Kaiju, Wang Wu |     |
| C7      | Chen Guoliang, He Chaodong, Yang Yixiang, Chen Chuanyong, Zhang Lianjie, Li Tingyin, Chen Dianxue, Wang Zuhui, Luo Gan, Lin Ximeng, Lin Shengduan, Li Shenzhi, Liang Shanjin, Zhang Keli, Fan Runshan, Qiao Picheng, Xu Shuping, Wu Jifan, Wang Zifu, Zhang Guiyuan, Luo Zhensheng, Qiao Pixian, Zhou Dunxian, Li Zhenmin, Li Shengyi, Li Jingan, Cao Dumou, Hu Zaiyu, Dong Chunshui, Meng Guangbin, Song Xuezeng, Yang Zhongfang, Cai Bolin, Fu Yisheng, Gao Xianying, Wei Zhaoqi, Yang Kairong, Lin Fulin, Lü Huanyi |     |
| C8      | Liu Bojian, Huang Shitao, Jiang Zemin, Xiong Weigeng                                                                                                                                                                              |     |
| C9      | Guo Qingzheng, Xie Zeyuan, Zuo Shaoxian, Zhu Zexiang, Dai Changzhen, Yang Zifu, He Luzhi, Li Huang, Luo Jingzhong, Kuang Hongru, Jian Lian, Feng Xuezong, Shen Shilin, Zheng Guoping, Zhou Yongsheng, Shi Limu, Zhang Xi, Chen Chongxian, Gan Rui |     |
| C10     | Nie Rongzhen                                                                                                                                                                                                                      |     |
| C11     | Chen Jie, Chen Hansheng, Chen Yinke                                                                                                                                                                                              |     |
| C12     | Chen Lu, Chen Xiongfei, Wang Yaoqun, Zhang Zhenhua, He Zehui, Liu Shuping, Ma Guangqi, Wang Bingnan, Chang Xiangyu, Li Bingde, Chen Dingmin, Li Shuhua, Zhang Lisheng, Chen Jiesheng, Carsun Chang, Chen Daqi, Chen Bangjie, Zhu Xi, Cao Gubing, Zhou Chuanru, Chen Cong, Xing Xiazhong |     |
| C13     | He Changgong, Xing Xiping                                                                                                                                                                                                         |     |
| C14     | Qian Sanqiang, Yan Jici, Chen Shoumin, Yin Zanxun                                                                                                                                                                                 |     |
| C15     | Xu Teli, Xu Deheng, Chen Jilie, Chen Panzo                                                                                                                                                                                        |     |
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
When trying to explore possible causes behind the various clustering seen in this paper, hierarchical cluster analysis of only the affiliations was undertaken to determine which affiliations were most similar to each other. Does the inclusion of these affiliations accord with the historical context? Examining HCA cluster 3, which includes only women, provides a micro-study of this question by examining the gender affiliation and its nearest neighbours. Five validity indices for cluster number were generated that recommended 12 HCA clusters as optimal. [Figure 9](#anchor-figure-9) shows only cluster 2-12 as cluster 1 was a relatively homogeneous cluster of all other affiliations.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 9: Excerpt of Hierarchical cluster analysis of CSE affiliations (affiliations=31)."], "type": "image"}} tags=["hermeneutics", "figure-9", "anchor-figure-9"]
library("IRdisplay")
display_png(file="./media/Fig9.png")
```

<!-- #region tags=["hermeneutics"] -->
The resulting dendrogram ([figure 9](#anchor-figure-9)) for affiliations can help explain which affiliations are similar to other affiliations. In this case, the affiliations have close ties with EGMD and IFCL (Sino-French Institute), Guangdong, and UTC (Charleroi) that were discussed in the nearest neighbour analysis ([Table 5](#anchor-table-5)). Also, in terms of understanding HCA cluster C3 ([Figure 8](#anchor-figure-8)), entirely composed of women, this affiliation analysis HCA ([figure 9](#anchor-figure-9)) shows some interesting information about the Cluster 3 eight women ([Table 6](#anchor-table-6)), out of sixteen females in the CSE dataset. The eight women represent various provincial origins - Hunan, Henan, Guangdong, Jiangsu, Liaoning – but not Sichuan. Some women matriculated at multiple universities.  These women experienced career paths that varied from educators in arts and sciences to becoming researchers. Wu Mengban, ( 吳孟班,1892-1970), born in Liaoning, obtained a doctorate at the University of Paris (1931), became an academic; Yuan Jianqin, (袁劍琴, b.1894 n.d.), born in Jiangsu, studied at the University of Beijing and University of Paris and became a painter; and Shu Zhihui (舒之銳, b. 1901 n.d.), born in Hunan, studied history in Montargis and University of Paris and became an academic. There was not a large influence of political affiliations - only the Fan cousins had a political affiliation (left-EGMD).
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
[Table 7](#anchor-table-7) shows the 28 affiliations for the women in cluster 3. All eight women identified themselves as work-study students. Five women studied at Montargis and four went to the IFCL. Interestingly, [figure 9](#anchor-figure-9) is another form of support for these similarities. The position of gender in Cluster 4 ([figure 9](#anchor-figure-9)) shows the most similar affiliations to gender are the work-study movement and Montargis College. Thus, using affiliation HCA confirms HCA of individuals and partly opens the door of looking at which affiliations are linked to which nearest neighbour affiliation and inclusion in which HCA cluster.
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 7: HCA Cluster # 3 Affiliations (N=28) Individuals (N=8)."], "type": "table"}} tags=["table-7", "hermeneutics", "anchor-table-7"] -->
| Affiliation                     | Number |
|---------------------------------|--------|
| Work Study Movement             | 8      |
| Montargis College               | 5      |
| IFCL                            | 4      |
| Hunan                           | 4      |
| U. Paris                        | 3      |
| EGMD                            | 2      |
| Acad Arts & Sciences            | 2      |
| Scientist                       | 2      |
| Lyons Univ                      | 2      |
| GMD Leftist                     | 2      |
| Educator                        | 2      |
| Educational Position            | 2      |
| Girls Normal School Beijing     | 2      |
| Jiangsu                         | 1      |
| Guangdong                       | 1      |
| Henan                           | 1      |
| Editor Position                 | 1      |
| Zhounan Girls Middle School     | 1      |
| Liaoning                        | 1      |
| New Citizens Study Society      | 1      |
| Academic                        | 1      |
| Artist Painter                  | 1      |
| Beijing Univ                    | 1      |
| École des Beaux-Arts Lyons      | 1      |
| École de chimie Lyon            | 1      |
| Natl School of Ag Montpellier   | 1      |
| Normal School Canton            | 1      |
| Univ of Dijon                   | 1      |
<!-- #endregion -->

While scholars will often remark on institutional ties and shared regional backgrounds, the political landscape has been more obscurely documented. How do these similarities reflect process of politicization in among the CSE individuals? The role of Europe as a backdrop for Chinese Communist Party branch development has been the most obvious focus, however, the vicissitudes of Europe as a backdrop for Guomindang politics is an exciting story and has many intriguing connections to the CSE group. The EGMD had three factions that mirrored the factions back in China. There was a right EGMD that was expelled by 1925 through the machinations of the left-Communist EGMD. In a reverse of political events to the China situation the ECCO actually had heavy leverage, if not control, of the EGMD through the mid-twenties (<cite data-cite="626961/GEVR2QEZ"></cite>). The EGMD generated numerous manifestos, public debates, and other activities. After the April 12th 1927 coup by Jiang Jieshi (蔣介石,1887-1975), there were massive protest meetings held among in the left-Communist EGMD community, with many French sympathizers in attendance. The left EGMD was closely aligned with Wang Jingwei, who was in France after 1927. Thus, the Wang Jingwei influenced left EGMD faction also broke off with the Communists after the Wuhan split in September 1927. The Communist EGMD persisted well after 1928. All three factions published the newspaper The Nation, (Guomin 國民), and the right EGMD also published The Three Principles, (Sanmin 三民). The newspaper orientations were detectable through the mastheads which had the Parisian addresses of publication. Thus, *3 rue Thouin* was the right EGMD; 31 rue des Écoles was the left EGMD, and 33 rue St. Jacques was the address of the Communist EGMD.


EGMD participation by the Chinese in the CSE group could be seen as influential, in particular the role of UTC student, Fang Ditang (mentioned above), who was praised by Wang Jingqi in the EGMD founding minutes in November 1923 as “the most important organizer of the Belgian section of the EGMD.” Fang also had organized eleven individuals to write a letter (conveyed by Wang) to the GMD Overseas Bureau attesting to their enthusiasm to join the GMD on June 23, 1923. Interestingly, Fang Ditang was expelled by the leftist-Communist controlled EGMD-ECCO United Front in August 1925 at a meeting chaired by twenty-one year old Deng Xiaoping, along with fourteen others for “treason to the party.” Among the fifteen expulsions, there were no IFCL members from the CSE group and two other UTC students, Yang Zifu (楊自福, n.d.), and Dai Chengzhen (戴昌震, n.d.). Fang Ditang later was listed as late as 1927 as on the EGMD roster of officials when they set up their own right EGMD faction (<cite data-cite="626961/CL4AYSZY"></cite>).


While Fang Ditang represented the right EGMD, Qiu Zhenggou (b. 1904) represented the standard left EGMD. Qiu was a graduate in sociology and literature at Paris University. He wrote for the EGMD newspaper, *The People* (Guomin), and became an EGMD leftist official. Qiu was a prominent educator in East and Southeast Asia. One of his articles about the Three People’s Principles, *Sanmin zhuyi* (三民主義) being a more inclusive ideology than Marxist class ideology asserted “The ideology of the GMD is the Three People’s Principles, a broad ideology that seeks national independence, the expansion of the people’s rights, and the enrichment of people’s lives. . . It is true that the GMD is a revolutionary party; but the GMD is not and should not be a party of peasant-workers. Looking at the history of the GMD, one can see that the GMD has been successfully organized by all revolutionary elements of each class that believe in the Three People’s Principles.” This is an example of the materials collected in the French colonial archives (<cite data-cite="626961/CL4AYSZY"></cite>, p. 197).


While many Left EGMD individuals have slipped into historical obscurity, one member who became prominent in the GMD government was IFCL student, Zheng Yanfen (鄭彥棻,1904-1990) who later became Minister of Justice in Taiwan. He wrote an important article, critiquing the Soviet Union in 1930 for the EGMD publication *La Voix du Kuomintang en Europe*, entitled “International Opinion on the Sino-Soviet Question and the Lessons it Can Give to Us.” After laying a foundation of theory and fact, Zheng analyzed sixteen different countries for their opinions on the Soviet Union (<cite data-cite="626961/CL4AYSZY"></cite>, pp.197-198).


In terms of the CSE group, there were radical groups at the IFCL who were monitored and sometimes expelled. Two cases aroused heated feelings in the summer and fall of 1927. These expulsions were requested of the IFCL by the rector of Sun Yatsen University in Guangdong, Zou Lu. The cases focused on Zhang Ruiju (張瑞矩, 1903-n.d.), who wrote a sympathetic article about oppressed sailors.  The Zhang Ruiju dossier at the IFCL has amazing documents, meetings with officials, protests by supportive IFCL students, and letters in support and against by institutional and government officials. A second key case involved “Johnson” Long (Long Zhanxing 龍詹興,1903-1985), and three others Peng Shiqin (彭師勤,1901-1979), Yan Jijin (顏繼金,1900-1966), and Xie Qing (謝清,1896-n.d.). Both cases have extensive documentation, and it seems clear that “Johnson” Long was seen by his teachers as an original thinker, had a buoyant personality, and was most probably a Communist sympathizer. In the case of Long, Peng, Yan, and Xie – they were accused of being Communists by Chinese students in Paris and Lyon and actually had been under surveillance by the Rhône Police since the summer of 1926, with a report in 1927 that listed several students who were suspected of being Communists. The dean at the IFCL, Jean Lépine, remarked that these students would indeed be expelled as the IFCL could not permit these views to exist at the Institut (<cite data-cite="626961/CL4AYSZY"></cite>, pp. 215-227).


The CSE data of students intertwined with so many others in a rich international environment. For some their education helped frame their learning towards a future as scholars and academics, as well as potential political intellectuals, while for others their extracurricular activities guided them towards different life pathways. For example, some IFCL students, following the path of the IFCL founders, became the most avid advocators of the Esperanto Movement that is intertwined with anarchist activities in early twentieth-century China (<cite data-cite="626961/MHMY2XCE"></cite>). The next section will examine the CSE group through the lens of network subgroup analysis.

<!-- #region tags=["hermeneutics"] -->
# Network Analyses of the CSE subgroups
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
Network analysis has greatly grown as a field, utilized by a wide array of disciplines in both theoretical and applied areas. According to Bonnie Erikson, in her pioneering article on network analysis and history:
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
*Network analysis is taking social structure seriously, that is, seriously enough to use the distinctive theoretical and technical tools required by the distinctive nature of structure. Although the term has many meanings, to a networker structure means the pattern of social relationships linking social actors. The actors may be people, organizations, positions within organizations, city-states, nations, families, and so on. The links may be friendship, hatred, trade, war, alliance, or any other relationship of interest. Whatever the substance of the network actors and ties among them, we can look at the network's structure with the same powerful set of tools; and we must use special tools. The methods in standard statistics books will not work, and neither will the theoretical positions that limit themselves to ideas that accompany standard analyses. . . Standard analyses use individual attributes of social actors, not social relationships among social actors*. (<cite data-cite="626961/33CBC5A6"></cite>, p. 2)
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
Network ties can be of several different types such as directed (communication going from A → B), undirected (no directionality known as is the case of binary data), and degree or strength of a tie. Additionally, network ties can and are often very temporally and spatially dynamic, which also describes many aspects of history. As stated above this work utilized an affiliation matrix which is very common in social network analyses and inevitably consists of two types of nodes (“two-mode”), i.e., individual node versus node affiliations. With affiliation matrices, network analysis is conducted in two manners. One, where different analytical methods are used for the two-mode data and secondly, the two-mode data is transformed into one-mode, i.e., individual x individual, by using different computational models. Centralities and subgroup analysis (Louvain) was used via two-mode while all other computations used one-mode. A limitation of two-mode is the far fewer available analytical procedures, however, there can be a conversion of two-mode to one-mode data that does allow many more additional analyses, but according to network theory there is some loss of data, but the results still are quite acceptable (<cite data-cite="626961/AM686FWS"></cite>, <cite data-cite="626961/GCY6JDUE"></cite>, <cite data-cite="626961/6WTHGN6Z"></cite>). There are many ways to convert two-mode data to one-mode data, and this analysis selected the sum of cross-products method and all network analyses done via UCINET (<cite data-cite="626961/EZUWUFT4"></cite>).
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
Network analysis allows for a level of processing that the brain could not easily perform. For example, in the network analysis below there are 197 individuals who are analyzed by the formula N*(N-1)/2 which equals 19,306 possible ties, requiring each individual being analyzed by that total amount of ties multiplied by the number of affiliations.
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
## Cohesion and Triad measures for the entire CSE group
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
This section discusses the entire CSE group network cohesion measurements. Network cohesion measures describe overall structure – that is what the network looks like in terms of density, average linkage or path length, size (radius, diameter) and transitivity. Density depends on network size and is simply the number of actual linkages present relative to the total theoretical maximum. Average path length is just the average number of steps along the shortest paths for all possible pairs of individuals which reveals an easily and quickly traveled network compared with a more complicated and inefficient network with a longer average path length. Diameter is the greatest distance between the two farthest individuals and gives a good indication of size as it describes the maximum number of links or steps to any individual. A network where any individual is only a few links from another individual is a very compact network. Lastly, transitivity essentially measures the probability that adjacent individuals have a transitive linkage which is shared among individuals, e.g., Li Pingheng<–>Chen Panzao<–> Zhang Bojun where Zhang has a connection to Li via Chen (a transitive link). Transitivity is related to average path length which is logical since if the average path distances are shorter, it is easier and quicker to connect to another node.
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 8:  Two-mode cohesion values for entire network and four smaller networks of only each institution attendees."], "type": "table"}} tags=["hermeneutics", "table-8"] -->
|                    | **Density** | **Average Distance** | **Radius** | **Diameter** | **Fragmentation** | **Transitivity** |
|--------------------|-------------|----------------------|------------|--------------|-------------------|-------------------|
| **Entire Network** | 0.048       | 2.889                | 3.000      | 6.000        | 0.005             | 0.494             |
| **IFCL**           | 0.091       | 2.821                | 3.000      | 6.000        | 0.000             | 0.570             |
| **UTC**            | 0.096       | 2.758                | 3.000      | 6.000        | 0.000             | 0.585             |
| **UP**             | 0.137       | 3.215                | 3.000      | 4.000        | 0.000             | 0.466             |
| **UB**             | 0.123       | 3.364                | 3.000      | 6.000        | 0.000             | 0.455             |
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
It is interesting that with four diverse institutions, in three countries, France, Belgium, and Germany, the total CSE network had a 0.048 density which is low (4.8% ties existed out of all possible ties) while the much smaller institution only networks were appreciably higher. By using comparative densities, it was discernible that UP had the highest proportion of possible ties followed closely by UB while UTC and IFCL were the lowest densities of the four institutions. These results match the average distances but with UP and UB higher indicating an extra step and lower transitivities matching the higher average longer distances. In summary Table 8 indicates that UP and UB had less connected individuals than the other two institutions. Using comparative densities is a one way to see aspects of different networks, even subnetworks (<cite data-cite="undefined"></cite>, p.175).
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
While analyzing networks at the highest levels as with cohesion, one can also explore networks at the lowest or minimal level, i.e., the triad, with only three nodes which is the smallest possible network. A triad census of the network also reveals differences in the educational institutions. A triad census enumerates all of the patterns of the actual links at the three-individual group level. In the CSE group the network ties are undirected, which means there are four possible triad types. For directed ties, there are an additional twelve triadic structure types. The articulation of triadic analysis structure was developed by Holland and Leinhardt (<cite data-cite="626961/V2QE6BIR"></cite>, <cite data-cite="626961/I6KYKRCD"></cite>). The triad types for undirected nodes are: 003 (isolation) that contain three isolated nodes; 102 where two nodes (pair) are not connected to the third; 201 (structural hole) where the third tie does not occur creating a hole in the network that may or may not be changed over time, and 300 (cluster) where three nodes are fully connected also creating a closed structure. The four types of undirected triadic relations are illustrated in [figure 10](#anchor-figure-10). In [figure 11](#anchor-figure-11) the four institutions are shown in a bar graph four these four types of triadic relationships as conducted in a triadic census of the CSE group, using the program Pajek.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 10: Four types of triadic analysis structures for undirected ties."], "type": "image"}} tags=["hermeneutics", "figure-10", "anchor-figure-10"]
library("IRdisplay")
display_png(file="./media/Fig10.png")
```

```R jdh={"object": {"source": ["figure 11: Institutional triad census of undirected ties for UB (Berlin), UTC (Charleroi), IFCL (Lyon), and UP (Paris). The four structure types include triad Type: 003 (isolation), 102 (pairs), 201 (structural holes) and 300 (clusters)."], "type": "image"}} tags=["hermeneutics", "figure-11"]
library("IRdisplay")
display_png(file="./media/Fig11.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
There are some distinctive differences between these four educational institutions. First the UB is mostly type 300 and 102, respectively with 72.9% and 17.9% (90.7% combined). The next institution is the UP with type 300 and 201, respectively with 71.6% and 21.7% (93.3% combined). The third institution IFCL also has types 300 and 201, respectively with 85.7% and 9.4% (95.2% combined). Lastly, UTC with type 300, 201, 102, and 003, respectively with 22.0%, 18.9%, 41.4%, and 17.7% (100% combined). UTC essentially is the only institution with many individuals (22%) not connected or there is simply missing data, while the others had zero to less than 1%. There are several things worth noting here: (a) both UP and UB have strong dominance of triad type 300 (clusters) but most of the remaining triads were either 201 (structural hole) or 102 (pair), (b) Lyon is almost all type 300 (cluster), (c) UTC has approximately equality between all four triad types. (d) all of the institutions except for UTC had essentially no type 003 (isolation).
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
The above suggests some interesting possibilities. One, both UB and UP had mostly individuals that were well linked and even the pair and structural hole triads may be nothing more than soon to be realized cluster triads or it may indicate difficulty in establishing further ties. Two, IFCL was even more connected with almost all cluster triads. Lastly, and perhaps most unusual is UTC with near equality in all triad types which may indicate many things beyond individual diversity due to highly dynamic and changing groups. On the other hand, it could be that there is less data for UTC or even for the other institutions that would change these results. These observations merit further exploration and analysis.
<!-- #endregion -->

<!-- #region tags=["hermeneutics"] -->
How might historians understand the links between individuals in triad patterns?  For example, only for the IFCL group (N=90, 95 affiliations) when one performs cluster analyses of both individuals and affiliations there are some patterns worth noting. In the hierarchical clustering of individuals, there is a distinctive clustering together of individuals that also reflect their similarities and differences. In [figure 12](#anchor-figure-12) dendrogram that shows individuals, the height point was at 66.6% yielding seven highly distinct clusters.  With one exception (C1), being Yang Kun (楊堃, 1901-1998), an outlier to cluster C2, the remaining clusters (two through seven) reflect the adopted political allegiances and/or academic pathways. For example, cluster two has key Communist-leaning and left EGMD and cluster four has key GYS members.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 12: Hierarchical clustering of IFCL group (N=90, 95 affiliations) by individuals (rows)."], "type": "image"}} tags=["hermeneutics", "figure-12", "anchor-figure-12"]
library("IRdisplay")
display_png(file="./media/Fig12.png")
```

<!-- #region tags=["hermeneutics"] -->
[Figure 13](#anchor-figure-13) is an HCA analysis of only IFCL affiliations with a height set at 21.5% resulting in 14 clusters. [Figure 13](#anchor-figure-13)  also supports the triad 300 (clusters) finding, with similarities between the affiliations of Young Catholic aid and the Social Democratic Party (C1).  The more radical affiliations such as CCP, Communist EGMD, and ECCO are in cluster two. [Figure 13](#anchor-figure-13)  also shows that linkages inside C2 and C3 that make up the bulk of the affiliations are fairly cohesive as seen in only gradually rising linkage levels rather than abrupt changes.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 13: Hierarchical clustering of IFCL group (N=90, 95 affiliations) by affiliations (columns)."], "type": "image"}} tags=["hermeneutics", "figure-13", "anchor-figure-13"]
library("IRdisplay")
display_png(file="./media/Fig13.png")
```

<!-- #region tags=["hermeneutics"] -->
While this section has explored the entire network and its patterns of cohesion and tie formations, with one focus study of the IFCL, the next two sections will analyse centrality measures and visualizations to delineate the importance of individual roles and relationships within the network structure.
<!-- #endregion -->

## Centrality Measures of the CSE group

<!-- #region tags=["hermeneutics"] -->
Networks frequently include key individuals who can be influential in several ways and identified by various methods. Centrality refers to a group of metrics that quantify the position of a node within a network in terms of number of ties and how those occur throughout for each node. The centrality measures utilized in the tables below include:

* Degree centrality which measures the number of links per individual. This is one way to determine the individual’s activity and high scores may indicate power and/or prestige.
* Eigenvector centrality indicates that an individual is connected to individuals who themselves are highly connected. These are individuals who are at the centers of significant power and important to potential collaborations.
* Closeness centrality measures how short all the links are to a specific node such that information may travel fastest through that node to other nodes throughout the network.
* Betweenness centrality measures the frequency to which individuals lie between other individuals similar to a turnstile that others must pass to get to another person. A high betweenness measure indicates a potential power broker in the network (<cite data-cite="626961/C7XYAC8R"></cite>, <cite data-cite="626961/EFN22MFF"></cite>).
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
In [Table 9](#anchor-table-9), Nie Rongzhen dominates the top centrality measures. His political experiences in Europe, affiliation with UTC, EGMD and ECCO leadership, later military, political, and government activities indicated that he was in fact the highest ranked in terms of potential influence. Nie had the highest numbers in both closeness and betweenness which means that he had high access to information and that he probably was a power broker. In the number of ties that he has as measured by degree, Nie Rongzhen has an astonishing Z-score of 6.613, which is over six standard deviations beyond the mean (a Z-score is the number of standard deviations), while the next person, He Changgong (何長工, 1900-1987) has a degree Z-score of 4.200. Nie Rongzhen has an even higher Z-score of 8.747 for betweenness centrality, which indicates he is someone most frequently found as a middleman so to speak in trying to reach others. A more in-depth study of Nie Rongzhen might allow a more detailed understanding of how CCP revolutionaries and intellectuals may have connected with someone when they shared an educational connection.
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 9:  Two-mode normalized centrality measures for the top 25 CSE individuals (N=197)."], "type": "table"}} tags=["hermeneutics", "table-9", "anchor-table-9"] -->
| **Individual** | **Degree** | **Individual** | **Eigenvector** | **Individual** | **Closeness** | **Individual** | **Betweenness** |
|----------------|------------|----------------|-----------------|----------------|---------------|----------------|-----------------|
| Nie Rongzhen   | 0,2        | Peng Xiang     | 0,140           | Nie Rongzhen   | 0,644         | Nie Rongzhen   | 0,082           |
| He Changgong   | 0,141      | Nie Rongzhen   | 0,139           | He Changgong   | 0,626         | He Changgong   | 0,049           |
| Xing Xiping    | 0,112      | Fan Xinshun    | 0,134           | Xiong Weigeng  | 0,61          | Yang Kun       | 0,033           |
| Xu Teli        | 0,107      | He Changgong   | 0,130           | Jiang Zemin_1  | 0,608         | Chen Jiesheng  | 0,027           |
| Yang Kun       | 0,107      | Peng Shiqin    | 0,129           | Fang Ditang    | 0,602         | Chen Jie_1     | 0,027           |
| Chen Jie_1     | 0,083      | Zheng Yanfen   | 0,126           | Liu Bojian     | 0,6           | Xing Xiping    | 0,025           |
| Chen Panzao    | 0,083      | Chen Shunong   | 0,122           | Xu Shuping     | 0,596         | Chen Panzao    | 0,024           |
| Xu Deheng      | 0,083      | Yan Jijin      | 0,122           | Fan Xinshun    | 0,593         | Carsun Chang   | 0,024           |
| Yan Jici       | 0,083      | Liu Wentao     | 0,120           | Yang Kairong   | 0,593         | Xu Teli        | 0,021           |
| Zhang Ruoming  | 0,083      | Zhang Bojun    | 0,116           | He Chaodong    | 0,592         | Zhang Ruoming  | 0,021           |
| Chen Jiesheng  | 0,078      | Zhang Ruoming  | 0,116           | Liu Mingyan    | 0,592         | Chen Lu        | 0,020           |
| Liu Bojian     | 0,078      | Liu Mingyan    | 0,114           | Peng Shiqin    | 0,592         | Chen Hansheng  | 0,018           |
| Qian Sanqiang  | 0,078      | Wang Shumei    | 0,114           | Zhu Zexiang    | 0,592         | Chen Dingmin   | 0,016           |
| Carsun Chang   | 0,073      | Cai Shichun    | 0,113           | Li Pingheng    | 0,591         | Zhou Chuanru   | 0,015           |
| Chen Shoumin   | 0,073      | Xiong Weigeng  | 0,112           | Wei Bi         | 0,591         | Wang Yaoqun    | 0,015           |
| Wei Bi         | 0,073      | Li Pingheng    | 0,111           | Zhang Bojun    | 0,591         | Chen Jilie     | 0,015           |
| Xiong Weigeng  | 0,073      | Jiang Zemin_1  | 0,110           | Chen Panzao    | 0,589         | Yan Jici       | 0,014           |
| Chen Hansheng  | 0,068      | Li Dan         | 0,110           | Peng Xiang     | 0,589         | Cao Gubing     | 0,014           |
| Fan Xinshun    | 0,068      | Yang Kun       | 0,110           | Xing Xiping    | 0,587         | Liu Bojian     | 0,013           |
| Jiang Zemin_1  | 0,068      | Di Fuding      | 0,108           | Fan Xinqun     | 0,586         | Xu Shuping     | 0,013           |
| Chen Jilie     | 0,063      | Fang Ditang    | 0,108           | Liu Wentao     | 0,586         | Chen Shoumin   | 0,013           |
| Chen Yinke     | 0,063      | Wei Bi         | 0,106           | Wang Shumei    | 0,586         | Qian Sanqiang  | 0,013           |
| Liu Mingyan    | 0,063      | Xu Teli        | 0,104           | Yan Jijin      | 0,586         | Chen Yinke     | 0,013           |
| Peng Xiang     | 0,063      | Long Zhanxing  | 0,104           | Chen Shunong   | 0,585         | Wei Bi         | 0,012           |
<!-- #endregion -->

<!-- #region tags=["narrative", "hermeneutics"] -->
In terms of centrality, it must be recognized that homophily or someone wanting to join a network has two major choices to make, i.e., choice based on preferential attachment and/or fitness of the individuals in the existing network (<cite data-cite="626961/NC72G6ZB"></cite>, <cite data-cite="626961/CHQ3QB8Y"></cite>). Possible preferences are many as are the factors that each individual evaluates in terms of “fitness.” The choices are complex and temporally dynamic. Nie might have been someone who might be called “preferential attachment,” where others see his power or via his fitness in factors such as leadership, influential connections, thinking, and therefore seek a relationship because of his relationship strengths. One suspects there are many cases where Nie Rongzhen mediated difficulties or helped individuals. An example was his relationship with Xiong Weigeng ( 熊渭耕, 1900-1976) whose wife appealed to Nie Rongzhen to help restore his reputation after his brutal treatment and death suffered at the hands of Red Guards during the GPCR. Although Xiong had introduced Nie Rongzhen, along with Liu Bojian (劉伯堅, 1895-1935 ), to the ECCO, Xiong Weigeng essentially had not participated in the CCP after 1927. Nie was critical to the later proclamation -- decades after they last saw each other that allowed Xiong Weigeng’s honor to be restored (<cite data-cite="626961/GRHFVVIB"></cite>).Finally, Xiong Weigong’s high centrality scores for degree, Eigenvector, and closeness should be noted, especially as he did not have a high number of affiliations in the data. This underlines the fact that network analysis is about mapping the rich dimensionality of relationships between individuals that is based on a social network analysis that can articulate the importance of individuals within a network, that otherwise might not be uncovered.  Network analysis can reveal in the case of an historically active and well-connected individual, like Nie Rongzhen, who understandably is at high levels of centrality measures, is on a plane with someone, who is at a relatively high level in some measures like Xiong Weigeng, who did not have the positions or later ties with Nie Rongzhen. Yet the story of Xiong’s death and restoration of his character was due to his earlier personal relationship with a powerful leader.
<!-- #endregion -->

<!-- #region tags=["narrative", "hermeneutics"] -->
An interesting feature of the centrality analysis is the strength of several spousal and in-law couples, given that marriage and kinship data were not used in the data analysis, in particular husband and wife, Zhang Ruoming (張若名,1902-1958) and Yang Kun, and cousins-in-law Fan Xinshun and Peng Xiang (whose wife Fan Xinqun also is highly ranked in closeness centrality). Zhang Ruoming and Yang Kun were political activists, and both joined and resigned from the ECCO in the 1920s. Zhang had been a prominent May Fourth feminist, a founder of the Self-Awakening Society in Tianjin, and was imprisoned for several months during the May Fourth Movement. She had arrived in France as a frugal-study student and wrote newspaper articles about the work-study movement under the pseudonym of Miss “V.” Zhang actually had been a founder of the ECCO but quit the party in 1924 after the departure of Zhou Enlai, with whom she had a romance. She then focused on her literary studies at the IFCL. Yang Kun was one of the first students to matriculate at the IFCL and became active in both the ECCO and the EGMD. In 1927, on the advice of his Paris teachers, he decided to give up his membership in the Communist Party. Yang studied at the Institute of Ethnology in Paris under Marcel Mauss and wrote a dissertation on the Chinese family in ancient times. Zhang Ruoming wrote an award winning thesis on André Gide, which the author read and highly praised her in a letter written in 1930. The couple married in 1930 and returned home to distinguished academic careers. Zhang became a well-known scholar in French literary studies, while Yang was a pioneer of early Chinese religion and the anthropology of minorities in China. Later during the Anti-Rightist Campaign, after being labeled a rightist, and her sons unable to attend college, sick in spirit and in declining health, Zhang Ruoming committed suicide. After Zhang’s suicide, Yang carried on with his work, even after his ethnographic field notes were destroyed by the Red Guards (<cite data-cite="626961/QDZE63DM"></cite>, <cite data-cite="626961/CL4AYSZY"></cite>, <cite data-cite="626961/I79R7FRJ"></cite> K. Yang, personal communication, October 14, 1985). He later continued on as a professor in Beijing, mentoring graduate students until his death at the age of 97.
<!-- #endregion -->

<!-- #region tags=["narrative", "hermeneutics"] -->
Yang Kun ranks high in three measures of centrality (degree, Eigenvector, and betweenness). His Z-scores in degree (0.107) and betweenness (3.151) centralities are very indicative of a connected and influential individual. It could be argued that these scores indicate a connection that reveals the nuances of intellectual, political, and social ties across the decades of revolution and state-building. For example in Yang Kun’s case, he needs a more fine-tuned analysis given his strong IFCL connections to people like Zeng Boliang, (曾伯良,1905-n.d.) the brother of Zeng Zhongming (曾仲鸣,1896-1939), who later became important to the Wang Jingwei’s government. The question of linkages among Wang Jingwei’s sphere of influence and IFCL graduates also needs greater attention for the interwar years and after 1940, especially as Wang stayed in France several times during this period. Zeng Boliang was reported as a “communist” in both internal documents at IFCL and in French police reports. Other secretaries at IFCL, in addition to Zeng Zhongming, such as Chu Minyi (褚民誼,1884-1946), also followed Wang Jingwei. It might be interesting to reflect that Wang was more of a Francophile than his competitor, Jiang Jieshi, and may have been influenced by French leaders he knew after the French surrender to the Germans in January 1940. Likewise the lifelong relationships that Zhang Ruoming had with close friends like Zhou Enlai, from both the Self-Awakening Society and the ECCO and EGMD participation needs greater exploration (<cite data-cite="626961/I79R7FRJ"></cite>).
<!-- #endregion -->

<!-- #region tags=["narrative", "hermeneutics"] -->
Peng Xiang’s position also is intriguing for his Eigenvector centrality, i.e. being close to highly connected individuals. His Z-score of 2.435 is the highest rate in this measure. His compatriots, wife, and sister-in-law also have high scores on one or more centrality. Mentioned in police reports, at the IFCL he had a famous fistfight with Chen Shunong (陳書農,1898-1970), which embarrassed the program. Both Peng and Chen were leaders of the left EGMD, but neither of them was expelled for political reasons (<cite data-cite="626961/CL4AYSZY"></cite>, pp. 110–114). Chen Shunong was expelled in 1927 for lack of attention to his studies. Peng Xiang graduated in sociology and became an academic dean at the Shanghai Labor University upon his return to China. His cousin-in-law, Fan Xinshun later participated in the Democratic Leagues and had an academic career with her science degree. She ranked very high in the closeness centrality which expresses the possibility of her influence through more close connections to more individuals. Finally, the leaders in the betweenness centralization are intriguing for the diversity of people from high-ranking CCP leaders to distinguished intellectuals and high-power third-party leaders. This category represents those who were positioned as power brokers. The next section further explores subgroup linkages through network internal measures.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
## Network Internal Measures for the CSE group and the Ego Network of Nie Rongzhen
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
The final network analysis measures for the CSE group are five visualizations that include the entire network and three subgroup clusters obtained by the Louvain method (<cite data-cite="626961/CHHA3MM6"></cite>) and the ego network for Nie Rongzhen. [Figure 14](#anchor-figure-14) displays a VOS (Visualization of Similarities) network view of the CSE group network, with three subgroups obtained through Louvain subgroup detection that illustrates the three main subgroups consisted of the IFCL students (red), the UTC students (green) and the UP and UB students (blue). Because of the need to reduce links from 66,536 ties to 14,689 to obtain a less obstructed three-dimensional view, some of the individuals are not visible deeper in or on the backside, and periphery individual isolates are not shown linked to others.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 14: CSE network (N=197) in one-mode analysis with 14,689 ties."], "type": "image"}} tags=["hermeneutics", "figure-14", "anchor-figure-14"]
library("IRdisplay")
display_png(file="./media/Fig14.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
Cluster one as displayed in [Figure 15](#anchor-figure-15) is an interesting mixture with the UP represented by green, the UB represented by squares and Eigenvector centrality represented by size. The most significant indicator for this subgroup is that although it has the least political party participation in Europe, it has the largest number of CCP members (N=12, 26%) of the cluster network, including Nie Rongzhen and He Changgong.  This inclusion of twelve CCP members is in contrast to subgroup two (primarily UTC) where the percentage of CCP individuals is 5%, and cluster three (IFCL) where the percentage is 1% CCP membership. In addition to the most important communists, this Louvain subgroup one also has the most important Democratic League and Third-Party leaders, like Carsun Chang, Zhang Bojun, and Qian Sanqiang. Interestingly, Qian’s wife He Zehui is on the periphery.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 15: Louvain subgroup one of CSE individuals (N=45) using Louvain subgroups with ties greater than two, with 9,982 ties, displaying UP by colour (green), UB by blue rims, CTU by triangle shape, and two-mode Eigenvector centrality by size."], "type": "image"}} tags=["figure-15", "hermeneutics", "anchor-figure-15"]
library("IRdisplay")
display_png(file="./media/Fig15.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
As displayed in [figure 16](#anchor-figure-16), cluster two of the CSE group (N=64) is mostly composed of individuals from UTC. The EGMD and ECCO are two of the highest affiliations of this cluster grouping at 22% (N=14) and 28% (N=18) of the individuals. Hunan, Sichuan and Guangdong students are arrayed in separate regions of the subgroup. Eigenvector centrality measures illustrate that there were few individuals who were potential high popularity individuals that were also connected to similar individuals, such as Fang Ditang, Jiang Zemin, and Xiong Weigeng who all show high values in this measure with Z-scores above 1.420.
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 16: Louvain subgroup two (N=64) with ties greater than two, with 9,282 ties, displaying Guangdong by colour red, Hunan by blue colour, Sichuan by green rims, EGMD participation by square shape, and two-mode Eigenvector centrality in size."], "type": "image"}} tags=["figure-16", "hermeneutics", "anchor-figure-16"]
library("IRdisplay")
display_png(file="./media/Fig16.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
With the exception of three students who matriculated at UP, eighty-five individuals in cluster three (see figure 17) of the SE group (N=88) belong to the students at the IFCL. The large amount of Guangdong students (N=30) represented by shape and the prevalence of the EGMD (N=53) by green colour. This subgroup also has eight Social Democrats and seven Anarchists. Yang Kun and Zhang Ruoming had the highest degree centralities in this cluster (Z-scores respectively 2.809 and 1.827), again, signifying the potential strengths of political activists. Peng Xiang, who ranked highest in the Eigenvector measure is at the centre of this cluster
<!-- #endregion -->

```R jdh={"object": {"source": ["figure 17: Louvain subgroup three (N=88) with ties greater than two, with 9880 ties, displaying EGMD participation by colour (green), Guangdong origin by shape (squares), and ECCO by blue rims, and degree centrality by size. Five individuals are not shown."], "type": "image"}} tags=["figure-17", "hermeneutics"]
library("IRdisplay")
display_png(file="./media/Fig17.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
The final network visualization is the ego-network of Nie Rongzhen in [figure 18](#anchor-figure-18). Besides focusing on an entire network, minimal internal components (triads), or network subgroups, a network analysis that focuses on an individual is termed an ego (Latin for “I”) network and all the immediate ties as alter egos, a term originally used by Cicero (106-43 BCE) as a second self or trusted friend. As classical scholar, S. C. Marchetti, outlined its origins, the term is related to:
<!-- #endregion -->

*[P]olitical friendship, expressed in terms of an accentuated affectivity. The affectivity of Cicero responds to a personal capacity of attraction in Caesar. The feeling of heartfelt friendship that Cicero expresses for Caesar is like an extreme form of the affectivity which could, in any case, be linked to Roman political friendship. The first words at the beginning, for us, of the direct epistolary dialogue between Cicero and Caesar indicate Caesar as his alter ego: fam. 7. 5. 1 "You can see how far I am convinced that you are another myself". Cicero considers Caesar as another myself because he will take care of "his own", and will heed the requests of his protégés, as he would himself.* (<cite data-cite="626961/WJDPEI7F"></cite>, p. 287) [Emphasis Mine]

```R jdh={"object": {"source": ["figure 18: Nie Rongzhen ego network with 112 individuals with ties greater than two with 111 ties in two-mode analysis. Red=Louvain cluster 3, Gray=Louvain cluster 2, and Green =Louvain cluster 1. Eigenvector values are shown by symbol size."], "type": "image"}} tags=["figure-18", "hermeneutics", "anchor-fogure-18"]
library("IRdisplay")
display_png(file="./media/Fig18.png")
```

<!-- #region tags=["hermeneutics", "narrative"] -->
[Figure 18](#anchor-figure-18) (Nie Rongzhen’s ego network) revealed the alters for Nie Rongzhen, along with their subgroup status in the entire CSE network. Nie Ronghen’s relationship to all three Louvain subgroups is evident. Although he attended UTC, the broad spread of his ties can be seen by the predominance of the UP, UB, and IFCL individuals. As mentioned above, Nie Rongzhen is a possible preferred attachment individual when popularity breeds popularity. This means as individuals considered their potential associations, Nie Rongzhen’s stature as a person of many ties, would make him attractive to an ever-widening circle, that appears to be demonstrated by both figures 15 and 18. This stature also is evident in other data studies from the CBD. Even compared with larger CCP subsets that include 133 and 55 individuals, Nie Rongzhen ranks higher in some centrality measures than leaders such as Deng Xiaoping, Zhu De (朱德, 1886-1976) and Liu Shaoqi (劉少奇, 1898-1969).
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 10: Some ego network basic measures: Size (size of ego network), Ties (number of ties), Density (ties/no. possible), Reach efficiency (2-step reach divided by max possible given degrees of alters), Broker (no. pairs not directly connected), Normalized Broker (broker/number of pairs), EgoBetweenness (betweenness in own ego network)."], "type": "table"}} tags=["hermeneutics", "table-10", "anchor-table-10"] -->
| Name          | Size | Ties  | Density | ReachEff | Broker | nBroker | EgoBet |
|---------------|------|-------|---------|----------|--------|---------|--------|
| He Changgong  | 194  | 28764 | 76.8228 | 0.6697   | 4339   | 0.2318  | 66.0541|
| Jiang Zemin_1 | 194  | 28764 | 76.8228 | 0.6697   | 4339   | 0.2318  | 66.0541|
| Nie Rongzhen  | 194  | 28764 | 76.8228 | 0.6697   | 4339   | 0.2318  | 66.0541|
| Xiong Weigeng | 194  | 28764 | 76.8228 | 0.6697   | 4339   | 0.2318  | 66.0541|
| Fang Ditang   | 193  | 28548 | 77.0402 | 0.6723   | 4178   | 0.2296  | 64.8588|
| Yang Kairong  | 192  | 28418 | 77.4924 | 0.6738   | 4178   | 0.2251  | 61.9975|
| He Chaodong   | 191  | 27934 | 76.9744 | 0.6796   | 4254   | 0.2303  | 64.1802|
| Xu Shuping    | 191  | 27934 | 76.9744 | 0.6796   | 4127   | 0.2303  | 64.1802|
| Liu Bojian    | 188  | 27284 | 77.6084 | 0.6877   | 3936   | 0.2239  | 60.2195|
| Zhu Zexiang   | 188  | 27396 | 77.9270 | 0.6864   | 3880   | 0.2207  | 58.9872|
| Yao Baozhi    | 126  | 15556 | 98.7683 | 0.9468   | 87     | 0.0123  | 0.9440 |
| Gao Xianying  | 69   | 4518  | 96.2916 | 1.9924   | 87     | 0.0371  | 1.9993 |
| Wei Zhaoqi    | 69   | 4518  | 96.2916 | 1.9924   | 47     | 0.0371  | 1.9993 |
| Lü Huanyi     | 66   | 4196  | 97.8089 | 2.1013   | 97     | 0.0219  | 2.4737 |
| Xing Xiazhong | 19   | 338   | 98.8304 | 6.7086   | 2      | 0.0117  | 0.1111 |
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
A preliminary analysis of ego networks for all CSE students was performed for sixteen basic ego network values with seven values seen in Table 10 along with fifteen individuals and their respective ego network values. These fifteen individuals are comprised of the top ten that had the highest values for size (number of individuals in that ego’s network) along with five individuals with the lowest size values in the CSE students.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
If one focuses on just Nie Rongzhen there are some revealing results. In [Table 10](#anchor-table-10) Nie Rongzhen had the highest number of alters (so also did three others have a high number of alters) which is not surprising given his degree and eigenvector centralities in Table 9. However, those top five individuals, including Nie, had the lowest densities among all CSE ego networks with the highest densities found at the bottom of the table at 22% higher. Since density is a measure of actual ties versus all possible ties, the high density individuals were using many more ties amongst their alters, which may have been necessary for individuals with fewer alters and/or it may be that Nie and similar individuals could function quite well with 22% fewer ties with their alters. The high density individuals match the far fewer ties. These five high density individuals also were far more efficient in reaching the maximal number of their alters as seen in the reach efficiency.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
Nie Rongzhen also is shown to be a strong broker, where a broker is an individual that serves as a “go-between” for all the alters in that ego network. The measurement for a broker is the number of alter pairs that are not connected and in Nie’s case it was 4,339 pairs or 15.1% of his ego network. The broker value can be normalized by dividing by the number of pairs and that column shows Nie at ten-fold stronger brokerage behaviour than the lowest individuals.
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
When examining the top ten brokerage individuals it was noted that they all attended UTC and when comparing all 197 CSE student ego networks it was found that 54 out of 67 UTC attendees (81%) had high brokerage levels. This is an intriguing result as it raises many questions since a high value indicates individuals that prefer to be “go-betweens” between their alters. When did this behaviour appear and what factors may be involved? Did UTC attract these individuals or did brokerage evolve in Europe?
<!-- #endregion -->

<!-- #region tags=["hermeneutics", "narrative"] -->
Lastly, we see ego betweenness within each ego network and Nie Rongzhen’s high betweenness is repeated here as it was for the entire CSE network where he was highest in [Table 9](#anchor-table-9). Clearly Nie utilized broker behaviour consistently and perhaps both Nie Rongzhen and Xiong Weigeng (who also had high brokerage) both used strong brokerage behaviour and may have recognized responsibilities to each other, even years later. In Egocentric analysis there is a process called activation of latent ties that looks likely to have operated when Nie Rongzhen helped to restore Xiong Weigeng’s legacy decades after their last contact. According to Perry, et.al., the latent power of the relationship “represents a crucial coping mechanism for individuals facing unfamiliar challenges and periods of elevated support need.”(<cite data-cite="626961/QDEKCN8K"></cite>, p. 249).
<!-- #endregion -->

# Conclusion: Academics, Activists, and Revolutionaries


Chinese students at four institutions were studied in this article: the Institut Franco-Chinois (IFCL), Université du Travail Charleroi (UTC), the Université de Paris (UP), and the Universität zu Berlin (UB), collectively called the CSE group (N=197). The article adopted a multiple but integrative approach, exploring these groups through historical narrative, quantitative, and network analyses. Although some of the data was sparse for some groups, the article developed the case for a linkage between academic culture and politics in the microcosm of important issues that surrounded these students, many of whom became political intellectuals, and some of whom became revolutionaries.


These Chinese students were engaged in education and politics abroad in Europe during a decade full of challenge and opportunity. They were encouraged by progressive elders in the work-study movement, who also specialized in educational enterprises like IFCL and the exchanges at UTC. Therefore, there were the worker-students who were predisposed to view their education in terms of factory labour and college to save the nation with what they would learn about the applied sciences or the realm of social sciences and the arts. The other group were those who wanted to attain their educational degrees with the idea that the social revolution of education, science, and the arts were more important than ideological commitment. The former group had individuals who became revolutionaries and the latter group had individuals who became political intellectuals. While the revolutionaries lived a life of danger, the political intellectuals were more rooted in the solidity of their professional careers in the halls of teaching and research institutions. The CSE group and issues of politicization and personal destiny, generational transitions, and the utility of an integrative approach to historical studies will be discussed in this conclusion.


## Political Intellectuals and Personal Destiny


The most significant fact of this small group study is that, even with limited data on the UTC, is that political participation affected the majority of these individuals in the CSE group who adopted a known political affiliation during their periods of study. From what is known of the political participation the CSE group had 71 EGMD, 37 ECCO, 8 SDP, 7 GYS, and 4 QND members. These students were active in a very dynamic swirl of political activities, while pursuing their studies. Members of the EGMD and ECCO also came under the scrutiny of the French police and even by French administrators. However, for members the GYS, SDP or the QND they did not appear to have suffered many consequences for their political party participation during their stay in Europe.


The April 12th Coup in 1927 and the later September split in Wuhan with the left GMD meant real choices had to be made by students who were in the ECCO or the EGMD. The ECCO lasted through the 1930s, but a large part of its members did not go through with their studies, and we know that between sixty and seventy individuals returned to China through the Soviet Union (<cite data-cite="626961/QI27W395"></cite>, <cite data-cite="626961/FYWJPIBU"></cite>). In fact, the most important ECCO activists after the late 1920s might have been Chinese mariners and other workers. During the crucial year of 1927 the ECCO and the Communist EGMD were still generating polemics and holding meetings under the leadership of a lively leader, Xia Ting (夏霆,1902-1989), who was expelled from France that year. Xia Ting was a major force behind the Communist EGMD and was expelled by the French in 1927 to Belgium. He then went to the Soviet Union to serve the Comintern at KUTV and Red Professor College (to study). Xia married a Russian woman and finally returned in 1954 through the mediation of Zhou Enlai.


For members of the EGMD 1927 was a turning point. As mentioned, the EGMD had split into three groups, based on ideological differences, the left, right, and Communist factions who all had newspapers, meetings, and public clashes with opposing factions. As the IFCL students were caught up in the 1927 turning point. Several students were expelled. Other students made choices as well to turn away from formal political affiliations. The case study mentioned above of Yang Kun’s life trajectory illustrates the difficult choices that Chinese students faced in their divided loyalties between political aspirations and personal destiny. As we saw, Yang was active in both the EGMD and was a member of the ECCO up until the fractured political environment of 1927. Although the Communists heavily influenced the EGMD through the Wuhan split in the fall of 1927, the IFCL students were vulnerable because the Chinese and French educational administrators at Sun Yatsen University who were actively anti-Communist and expelled students suspected of Communist affiliation. Yang had fallen in love with Zhang Ruoming, who had quit the ECCO in 1924 after a contretemps with ECCO leadership after Zhou Enlai departed. Yang also was heavily influenced by his prestigious professors, such as Marcel Granet and Marcel Mauss, who believed in Yang Kun’s academic future. In an interview in 1990, Yang discussed how difficult the decision process was for him. When he made the decision to withdraw in the summer of 1927, the ECCO sent someone to convince him to stay. He was told that between the choice of academic and revolutionary that “there was no third road.” According to Yang, he deliberately missed a meeting the following day because of his discomfort with the idea of abandoning his political participation because he valued his academic future more. Yang and Zhang later became involved in Democratic Leagues and their work exemplified political activism by pioneering new scholarly methods and ideas. They became political intellectuals. The couple suffered through the anti-intellectual campaigns that, as was mentioned, caused the suicide of Zhang Ruoming, and yet Yang was able to survive and during his later years Yang Kun was allowed to rejoin the CCP. In his interview on this change, Yang asserted his visitor was Deng Xiaoping. The date of 1927 was discussed in detail with Yang and his son at this interview. They insisted that Deng was in Europe for an international conference. There were at least two famous anti-imperialist conferences being held at that time, so it might be possible.


Nie Rongzhen had academic aspirations to become a chemist. Although Nie was closely aligned with his Jiangjin, Sichuan set of friends, he also made broader contacts and was seen as a leader by those contacts, who encouraged him to join the ECCO. Ultimately, Nie Rongzhen made a conscious decision to abandon his studies and become a revolutionary. His contributions as a revolutionary in the realms of political, military, and post-1949 administrative leadership were manifold, and this is reflected in both his unique positions in the cluster and network analyses (X. Li, personal communication, October 25, 1985) (<cite data-cite="626961/EYP3RMGJ"></cite>).


## Generational Issues and Political Intellectuals


Political intellectuals were energized by the New Culture age and transnational cultural explorations shaped by European characteristics and Chinese perceptions of Europe. Certainly, the generation born between 1895 and 1906, as evidenced in this study demonstrated a dynamic of national purpose and a genuine openness to identity transformation. The social network analysis demonstrated that the impact of provincial origin, birth city, and birth year were intertwined with choices on work-study, frugal-study, and how seriously to pursue their education. Clearly, within the CSE group, the biggest contingent decided to focus on their studies with only 5% joining the revolutionaries, 5% becoming political leaders, and we know at a minimum, 38% joined the academic profession.


However, study of the CSE group also is intriguing for another generational issue that needs exploration. What was the result of these intellectual and political dynamics on the promoters of these educational enterprises (i.e., the older generation)? In particular, how was Cai Yuanpei influenced by his encounters with unruly work-study students, who he was willing to leave in the lurch during his pronouncements of withdrawing financial support from in early 1921? What were his priorities? It would seem that Cai Yuanpei had growing enthusiasm during the 1920s for the French form of higher education as evidenced from the history of the IFCL which stressed the superior educational objectives, the establishment of the Sino-French University campus in Beijing, and as Ruth Hayhoe has outlined, the incorporation of the French Grandes Écoles framework that Cai wanted to utilize to organize for Chinese higher education in the late 1920s (<cite data-cite="626961/D7YWQNYV"></cite>). Given that Cai had spent many years in Germany as well as France, his enthusiasm for the French model is an area that is intriguing in terms of how French culture impacted his views.


On the other side of the scale of these “giants” of Chinese twentieth century education, there is the case of Wang Jingwei, who like Cai Yuanpei, was particularly influenced by the French during the 1920s. In fact, Wang’s influence on the IFCL was to encourage the left EGMD, even after the Wuhan split of 1927. The EGMD newspapers published Wang’s views of how to create a more egalitarian economy and society. Handwritten articles were mimeographed such as “Yige genben guannian” (一個根本觀念, A Fundamental Concept) and other justifications for the break with the CCP and Jiang’s GMD (<cite data-cite="626961/GEVR2QEZ"></cite>, <cite data-cite="626961/CL4AYSZY"></cite>, <cite data-cite="626961/X9J4IWJL"></cite>).Some French diplomats, after the death of Sun Yatsen in 1925, had judged that Wang Jingwei was the perfect leader for the GMD and his relations remained strong with France. Wang Jingwei went to France and stayed in Paris and Lyon after the Wuhan split. Although Wang negotiated with the Japanese on a possible collaborationist government in the late 1930s, was it just a coincidence that his actual date of collaboration occurred after the French surrender to the Germans in January 1940? Was there any communication that encouraged this collaboration on either the Chinese or French side that recognized the strength of a previous relationship? How helpful to Wang in coordinating a collaborationist government were the ties of the administrators and students from the IFCL as well as other Chinese officials having served long years in France? At least three of these people, Zeng Zhongming, Chen Lu, and Chu Minyi worked for Wang in the collaborationist regime. The Wang Jingwei-Vichy ties need greater clarity, especially given France’s enormous interest in their Indochina colony. Wang may have served a key bridging role in the dual colonial yoke of Japan and France in Indochina during WWII. Why did Wang Jingwei go to Hanoi during this period of time? How was Wang helped by the Chinese then in France and returnees from France? The lines of transcultural influence and of the personal networks as outlined in this study suggest that these ties mattered not only to the younger generation but would be useful to explore for the older generations, especially at the turning points of 1927 and 1940.


## An Integrative Approach to Chinese Political History


Even with limited data for some of these institutions the number of individuals (N=197) and affiliations (N=205) help to increase our understanding of Chinese political history. One of the advantages of using quantitative, multivariate, geospatial, and network analyses is that it allows the historian to view both the individual and the group levels of history. For example, provincial affiliations such as Guangdong, were examined as to how they related to the specific institutions. The fact that Guangdong played almost no role in the UP and UB groups as illustrated in the provincial analysis and as displayed in Louvain subgroup one was significant because this group had the largest percentage of CCP members. Perhaps the Guangdong individuals tended to be more conservative or to follow the left EGMD. It is just as significant that the IFCL had the largest contingent of Guangdong individuals, who constituted 35% of the IFCL group and included only one revolutionary out of 88 individuals in the Louvain cluster.


The hierarchical clustering revealed some interesting similarities and differences between individuals and between HCA clusters. The HCA clusters tended to reflect educational and political affiliation. Sometimes the political affiliation took precedence over provincial or educational affiliation as was the case of two prominent Communists He Changgong (Hunan, UTC) and Xing Xiping (邢西萍,1903-1972 Hebei, UB), who are in a two-person cluster together. The issue of how affiliations could affect membership in various sectors was studied in a microstudy of cluster 3 that included only women. These women were further studied through an affiliation dendrogram figure 9 and an affiliation Table 8 for cluster 3. HCA also was used to examine both hierarchical structure of individuals and common affiliations for the IFCL, with figures 12 and 13 helping to interpret triad structures in the network. Network visualizations also highlighted the importance of multiple affiliations and the distinctive nature of social networks and connections beyond provincial origins and educational backgrounds. Another example of integrative history was the case study of Nie Rongzhen, who became a key leader of the Chinese 1949 Revolution. In particular the network analyses suggested his importance with several different measures. As stated by Perry, et. al., in their work, *Egocentric Network Analysis: Foundations, Methods, and Models*:


*A network perspective allows for, and even calls for, multimethod approaches. Any notion that there is only one way to approach understanding the nature, functioning, and effects of network ties is outdated and inefficient. There is no doubt that mathematical and quantitative research powerfully describes the structure of networks and documents whether their effects are significant or not., in a statistical sense. However, only by tapping into qualitative research can we escribe the “on the ground” mechanisms of network process and functioning.* (<cite data-cite="626961/QDEKCN8K"></cite>, p. 12)


In conclusion, this study has suggested new ways to view individual and group prosopography. However, further research should consider multiple approaches that can be integrative, exploring the CSE group and related institutions with more detailed evidence types, broader scope of prosopography, and multiple views and techniques from the individual to the group level.

<!-- #region jdh={"module": "object", "object": {"source": ["table 11: List of Abbreviations Including Affiliation Groups."]}} tags=["table-11", "anchor-table-11"] -->
| **Full name**                                              | **Abbreviation** |
|------------------------------------------------------------|-----------------|
| Chinese Biographical Database                              | CBD             |
| Chinese Students in Europe                                 | CSE             |
| Institut Franco-Chinois de Lyon                            | IFCL            |
| Université du Travail Charleroi                            | UTC             |
| Université de Paris                                        | UP              |
| Universität zu Berlin                                      | UB              |
| Anarchist Party (Surplus Society)                          | GYS             |
| European Branches of the   Chinese Communist Organizations | ECCO            |
| Chinese Social   Democratic Party                          | SDP             |
| European Branch of the   Chinese Nationalist Party         | EGMD            |
| Chinese Youth Party                                        | QND             |
| Great Proletarian   Cultural Revolution                    | GPCR            |
<!-- #endregion -->

<!-- #region jdh={"object": {"source": ["table 12: CSE Individual Pinyin names and characters."], "type": "table"}} tags=["table-12", "anchor-table-12"] -->
| **Name in pinyin** | **Name in Chinese** | **Name in pinyin** | **Name in Chinese** | **Name in pinyin** | **Name in Chinese** |
|:------------------:|---------------------|:------------------:|---------------------|:------------------:|---------------------|
| Cai Bolin          | 蔡泊霖              | Lai Guogao         | 賴國高              | Wu Mengban         | 吳孟班              |
| Cai Shichun        | 蔡時椿              | Li Bingde          | 李秉德              | Wu Wenan           | 吳文安              |
| Cao Dumou          | 曹度謀              | Li Dan             | 李丹                | Xiao Zhensheng     | 蕭振聲              |
| Cao Gubing         | 曹谷冰              | Li Guocai          | 黎國材              | Xie Qing           | 謝清                |
| Cao Qingtai        | 曹清泰              | Li Hao             | 李淏                | Xie Zeyuan         | 謝澤沅              |
| Cao Xisan          | 曹錫三              | Li Huang           | 李璜                | Xing Xiazhong      | 邢俠忠              |
| Carsun Chang       | 張君勱              | Li Jingan          | 李敬安              | Xing Xiping        | 邢西萍              |
| Chang Xiangyu      | 常香玉              | Li Lianggong       | 李亮恭              | Xiong Weigeng      | 熊渭耕              |
| Chen Bangjie       | 陳邦杰              | Li Pingheng        | 李平衡              | Xu Dahong          | 徐大鴻              |
| Chen Chongxian     | 陳崇憲              | Li Qijue           | 李其玨              | Xu Deheng          | 許德珩              |
| Chen Chuanyong     | 陳傳詠              | Li Shengyi         | 李繩彝              | Xu Shuping         | 徐樹屛              |
| Chen Cong          | 陳琮                | Li Shenzhi         | 李慎之              | Xu Teli            | 徐特立              |
| Chen Daqi          | 陳大齐              | Li Shixiong        | 李世雄              | Yan Jici           | 嚴濟慈              |
| Chen Dianxue       | 陳典學              | Li Shuhua          | 李書華              | Yan Jijin          | 顏繼金              |
| Chen Dingmin       | 陳定民              | Li Tingyin         | 李庭陰              | Yang Chao          | 楊超                |
| Chen Guoliang      | 陳國樑              | Li Zhenmin         | 李振民              | Yang Gengtao       | 楊賡陶              |
| Chen Hansheng      | 陳翰笙              | Liang Shanjin      | 梁善金              | Yang Jie           | 楊傑                |
| Chen Jie_1         | 陳介                | Liang Tianyong     | 梁天咏              | Yang Kairong       | 楊開榮              |
| Chen Jiesheng      | 陳介生              | Lin Fulin          | 林福霖              | Yang Kun           | 楊堃                |
| Chen Jilie         | 陳繼烈              | Lin Shengduan      | 林聖端              | Yang Qian          | 楊潛                |
| Chen Lu            | 陳籙                | Lin Ximeng         | 林希孟              | Yang Runyu         | 楊潤餘              |
| Chen Panzao        | 陳泮藻              | Liu Bojian         | 劉伯堅              | Yang Yixiang       | 楊一香              |
| Chen Shaoyuan      | 陳紹源              | Liu Chong          | 劉充                | Yang Zhongfang     | .                   |
| Chen Shoumin       | 陳壽民              | Liu Keping         | 劉克平              | Yang Zifu          | 楊自福              |
| Chen Shunong       | 陳書農              | Liu Mingyan        | 劉明儼              | Yao Baozhi         | 姚保之              |
| Chen Xiongfei      | 陳雄飛              | Liu Puqing         | 劉圃青              | Ye Yunli           | 葉蘊理              |
| Chen Yinke         | 陳寅恪              | Liu Shixin         | 劉石心              | Yin Zanxun         | 尹贊勛              |
| Cheng Hongshou     | 程鴻壽              | Liu Shuping        | 劉樹屏              | Yuan Jianqin       | 袁劍琴              |
| Cui Zaiyang        | 崔載陽              | Liu Wentao         | 劉文濤              | Yuan Zhenying      | 袁振英              |
| Dai Changzhen      | 戴昌震              | Liu Wu             | 劉梧                | Yuan Zhuoying      | 袁擢英              |
| Deng Kaiju         | 鄧開舉              | Long Yin           | 龍吟                | Zeng Boliang       | 曾伯良              |
| Di Fuding          | 狄福鼎              | Long Zhanxing      | 龍詹興              | Zeng Yi            | 曾義                |
| Dong Chunshui      | 凍春水              | Lü Huanyi          | 呂煥義              | Zhai Junqian       | 翟俊千              |
| Fan Huiguo         | 范會國              | Lu Xiafei          | 陆霞飞              | Zhang Bojun        | 章伯鈞              |
| Fan Runshan        | 樊潤山              | Luo Gan            | 羅幹                | Zhang Delu         | 張德錄              |
| Fan Xinqun         | 范新群              | Luo Jingzhong      | 羅竟中              | Zhang Guiyuan      | 張貴源              |
| Fan Xinshun        | 范新順              | Luo Zhensheng_1    | 羅振聲              | Zhang Keli         | 張克理              |
| Fan Ying           | 范櫻                | Ma Guangchen       | 馬光晨              | Zhang Lianjie      | 張聯捷              |
| Fang Ditang        | 方棣棠              | Ma Guangqi         | 馬光啓              | Zhang Lisheng      | 張厲生              |
| Feng Xuezong       | 馮學宗              | Meng Guangbin      | 孟廣斌              | Zhang Nong         | 張農                |
| Fu Chuanbo         | 符傳缽              | Nie Rongzhen       | 聶榮臻              | Zhang Ruiju        | 張瑞矩              |
| Fu Lun             | 傅綸                | Ou Shengbai        | 區聲白              | Zhang Ruoming      | 張若名              |
| Fu Yisheng         | 傅逸生              | Ouyang Tai         | 歐陽泰              | Zhang Tong         | 章桐                |
| Gan Rui            | 甘瑞                | Peng Shiqin        | 彭師勤              | Zhang Wenjia       | 張文甲              |
| Gao Xianying       | 高憲英              | Peng Xiang         | 彭襄                | Zhang Wuyuan       | 張務源              |
| Guo Qingzheng      | 郭清正              | Qian Sanqiang      | 錢三強              | Zhang Xi           | 張熙                |
| Han Luchen         | 韓旅塵              | Qiao Picheng       | 喬丕成              | Zhang Yun          | 張雲                |
| He Changgong       | 何長工              | Qiao Pixian        | 喬丕顯              | Zhang Zhenhua      | 張振華              |
| He Chaodong        | 何朝棟              | Qiu Zhengou        | .                   | Zhao Yangxuan      | 趙仰玄              |
| He Chichang        | 何熾昌              | Shang Wu           | 黃巽                | Zhao Yanlai        | 趙雁來              |
| He Jingqu          | 何經渠              | Shen Shilin        | 沈士麟              | Zheng Dazhang      | 鄭大章              |
| He Luzhi           | 何魯之              | Shi Limu           | 師立木              | Zheng Guoping      | 鄭國平              |
| He Yanxuan         | 何衍璿              | Shu Hong           | 舒宏                | Zheng Shiyan       | 鄭士彥              |
| He Zehui           | 何泽慧              | Shu Zhirui         | 舒之銳              | Zheng Yanfen       | 鄭彥芬              |
| He Zhaoqing        | 何兆清              | Song Xuezeng       | 宋學曾              | Zhou Chonggao      | 周崇高              |
| Hou Jinxiang       | 侯晋祥              | Tang Xueyong       | 唐學詠              | Zhou Chuanru       | 周傳儒              |
| Hu Zaiyu           | 胡在獄              | Wang Bingnan       | 王炳南              | Zhou Dunxian       | 周敦憲              |
| Hua Lin            | 華林                | Wang Deyao         | 汪德耀              | Zhou Faqi          | 周發歧              |
| Huang Shitao       | 黄士韬              | Wang Shumei        | 王樹梅              | Zhou Song          | 周松                |
| Huang Xun          | 黃巽                | Wang Wu            | 王武                | Zhou Yongsheng     | 周永生              |
| Huang Ye           | 黄葉                | Wang Yaoqun        | 王耀群              | Zhu Xi             | 朱洗                |
| Huo Jinming        | 霍金銘              | Wang Zifu          | .                   | Zhu Yancheng       | 朱彥丞              |
| Jian Lian          | 簡廉                | Wang Zuhui         | 王組輝              | Zhu Zexiang        | 朱澤祥              |
| Jiang Zemin_1      | 江澤民              | Wei Bi             | 魏璧                | Zhu Zhenwu         | 朱振武              |
| Jin Shuzhang       | 金樹章              | Wei Zhaoqi         | 魏兆淇              | Zuo Shaoxian       | 左紹先              |
| Kuang Hongru       | 况鸿儒              | Wu Jifan           | 吳季藩              |                    |                     |
<!-- #endregion -->

<!-- #region tags=["hidden"] -->
# Bibliography
<!-- #endregion -->

<!-- #region tags=["hidden"] -->
<div class="cite2c-biblio"></div>
<!-- #endregion -->

<!-- #region tags=["hidden"] -->
Type Markdown and LaTeX:  𝛼2
<!-- #endregion -->

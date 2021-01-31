# AMiCo 

In this work, we present AMiCo, a wide-coverage and carefully designed cross-lingual and multilingual evaluation set; it aims to assess the ability of state-of-the-art representation models to reason over cross-lingual lexical-level concept alignment in context for 14 language pairs. Compared to related tasks such as [WiC](https://pilehvar.github.io/wic/) and [XL-WiC](https://pilehvar.github.io/xlwic/), our dataset offers

1. wide coverage of **diverse languages** and unique words
2. higher quality with **higher human performance** (around 90\%, compared with 80\% in WiC and XL-WiC)
3. **more challenges** as we introduce adversarial examples and more careful data extraction strategies
4. explicit **cross-lingual** evaluation

## Languages

English (EN), German (DE), Russian (RU), Japanese (JA), Korean (KO), Mandarin Chinese(ZH), Arabic(AR), Indonesian(IN), Finnish(FI), Turkish(TR), Basque(EU), Georgian(KA), Urdu(UR), Bengali(BN), Kazakh(KK).

## Data format
You will find train, dev and test tsv files in each language folder in `./data`. A data example consists of two word in context instances coming from English and another target language. The system needs to predict whether the two target words in context have the same meaning ("T") or not ("F"). Below are some examples from the ZH train.tsv:

| context1 | context2 | label  |
|---|---|---|
| 泰坦系列导弹的发射任务结束后，LC-16被移交给NASA用做双子座计划的航天员训练及  \<word\>阿波罗\</word\> 中飞船服务舱的静态试车。发射场再次回到空军手中是1972年，军方将其改造后用于潘兴导弹发射，导弹于1974年5月7日首飞。|  Bill Kaysing ( July 31 , 1922 – April 21 , 2005 ) was an American writer who claimed that the six  \<word\>Apollo\</word\> Moon landings between July 1969 and December 1972 were hoax es , and so a founder of the Moon hoax movement .   |     T
| 阿波罗-联盟测试计划中，美国的  \<word/\>阿波罗\</word\> 航天器和苏联的联盟航天器在地球轨道中对接。联盟号航天器有正式的任务名：联盟19号，而阿波罗航天器则没有正式的名称，但也在少数场合被称为“阿波罗18号”，尽管这是错误的叫法。  |  The Lunar Orbiter 3 was a spacecraft launched by NASA in 1967 as part of the Lunar Orbiter Program . It was designed primarily to photograph areas of the lunar surface for confirmation of safe landing sites for the Surveyor and  \<word\>Apollo\</word\> missions . It was also equipped to collect selenodetic , radiation intensity , and micrometeoroid impact data . | F  |
|泰坦系列导弹的发射任务结束后，LC-16被移交给  \<word\>NASA\</word\> 用做双子座计划的航天员训练及阿波罗中飞船服务舱的静态试车。发射场再次回到空军手中是1972年，军方将其改造后用于潘兴导弹发射，导弹于1974年5月7日首飞。|  Bill Kaysing ( July 31 , 1922 – April 21 , 2005 ) was an American writer who claimed that the six  \<word\>Apollo\</word\> Moon landings between July 1969 and December 1972 were hoax es , and so a founder of the Moon hoax movement .   |     F|


The target words in two contexts are marked with \<word\> \</word\>. 


---
title: Human Resourcesin julkistamisen valmistelu
description: Tällä sivulla on ohjeita Dynamics 365 Human Resourcesin julkaisemisen valmisteluun.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df2c55a8a69efa20c6d8c41e97c9e1f80ee1640d
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892750"
---
# <a name="prepare-for-human-resources-go-live"></a>Human Resourcesin julkistamisen valmistelu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resources -projektin julkistamisen valmistelua Microsoft Dynamics Lifecycle Servicesin (LCS) avulla. 

Tässä kuvassa on kaikki julkistamisprosessin vaiheet. 

![Julkistamisprosessi](./media/hr-admin-go-live-prepare-process.png)

Seuraavassa taulukossa on kaikki prosessin vaiheet, odotettu kesto ja kuka vastaa toiminnosta.

| Vaihe | Toimenpide | Kesto/ajankohta | Tekijä | Muistiinpanot |
| --- | --- | --- | --- |--- |
| 1 | Julkaisupäivämäärän päivitys LCS:ssä | Viimeistään 2–3 kuukautta etukäteen | Kumppani/asiakas | Välitavoitepäivämäärät on pidettävä ajan tasalla koko ajan. |
| 2 | Tarkistusluettelon viimeistely ja lähettäminen | Käyttäjän hyväksyntätestauksen (UAT) valmistumisen jälkeen | Kumppani/asiakas | Noudata [FastTrackin julkaisuarvioinnissa](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment) olevia ohjeita. |
| 3 | Projektin arviointi (FasTrack) | FasTrack-arkkitehti * | Arkkitehti toimittaa arvioinnin tarkistusluettelon vastaanottamisen jälkeen ja jatkaa arviointia, kunnes mahdolliset kysymykset on selvitetty ja korjaavat toimet on ilmoitettu. |
| 4 | Projektityöpaja (FasTrack) | FasTrack-arkkitehti * | |
| 5 | Tietopaketin tuonnit | Määräytyy projektin mukaan | Kumppani/asiakas | Noudata kohdassa [Tietojen hallinnan yleiskatsaus](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) olevia ohjeita.|
| 6 | Tuotantovalmius | Kaikkien edeltävien vaiheiden valmistumisen jälkeen | Kumppani/asiakas | Kumppani/asiakas ottaa vastuun tuotantoympäristöstä.|
| 7 | Valmistelusiirron aktiviteetit | Määräytyy projektin mukaan | Kumppani/asiakas | |
| 8 | Julkaisu | Määräytyy projektin mukaan | Asiakas | |

> [!IMPORTANT]
> *Vaiheet 3 ja 4 suoritetaan vain FastTrack-asiakkaille.

## <a name="completing-the-lcs-methodology"></a>LCS-menetelmän päättäminen

Jokaisen käyttöönottoprojektin tärkeä välitavoite on valmistelusiirto tuotantoympäristöön. Osavaiheen päättämisprosessissa on kaksi osaa: 

- Varsinaisen tehtävän, kuten sovitus- ja aukkoanalyysin tai käyttäjän hyväksyntätestauksen, suorittaminen. 
- Vastaavan osavaiheen merkitseminen suoritetuksi LCS-menetelmässä. 

On hyvän käytännön mukaista suorittaa menetelmän osavaiheet toteutuksessa edetessä. Ei siis kannata odottaa viime hetkeen saakka. Asiakkaan kannalta on järkevintä, että toteutus suoritetaan huolellisesti. 

## <a name="uat-for-your-solution"></a>Ratkaisun käyttäjän hyväksyntätestaus

Käyttäjän hyväksyntätestausvaiheen aikana on testattava kaikki toteutetut liiketoimintaprosessit ja mahdolliset mukautukset eristysympäristön toteutusprojektissa. Julkaisun onnistumisen varmistamiseksi seuraavat kannattaa ottaa huomioon käyttäjän hyväksyntätestausvaihetta suoritettaessa: 

- Suosittelemme, että hyväksyntätestausprosessi alkaa puhtaasta ja tyhjästä ympäristöstä, jossa GOLD-konfiguraatiosi tiedot kopioidaan ympäristöön ennen hyväksyntätestausprosessin aloittamista. On suositeltavaa käyttää tuotantoympäristöä GOLD-ympäristönä siihen asti, kunnes julkaiset ratkaisun, jolloin ympäristöstä tulee tuotanto.
- Testitapaukset kattavat kaikki tarpeet. 
- Testaus siirrettyjen tietojen avulla. Tämän tulisi siältää tietoja, kuten työntekijät, työt ja toimet. Lisäksi kannattaa sisällyttää alkusaldot, kuten loma-ja poissaolojaksotukset. Myös avoimia tapahtumia, kuten ajankohtaisia eturekisteröintejä, on syytä sisällyttää. Testaukseen kannattaa käyttää kaiken tyyppisiä tietoja, vaikka tietojoukkoa ei olisi viimeistelty. 
- Testaus käyttämällä oikeita käyttäjille määritettyjä käyttöoikeusrooleja (oletusroolit ja mukautetut roolit). 
- Varmistus, että ratkaisu noudattaa kaikkia yritys- ja toimialakohtaisia lakisääteisiä vaatimuksia. 
- Kaikkien ominaisuuksien dokumentointi sekä hyväksynnän ja kuittauksen hankkiminen asiakkaalta. 

## <a name="mock-go-live"></a>Julkistamisen harjoitus

Ennen kuin siirryt liveen, sinun on suoritettava julkaisun harjoitus, jotta voit testata vaiheita, joita on suoritettava, kun siirryt vanhoista järjestelmistä uuteen järjestelmään. Suorita julkaisun harjoitus eristysympäristössä, ja sisällytä kaikki vaiheet käyttöönottosuunnitelmaan.

- On suositeltavaa käyttää tuotantoympäristöä GOLD-konfiguraatioympäristönä julkaisuun saakka.
- Varmista, että tuotantoympäristöä suojataan vahvalla hallintoprosessilla vahingossa tehtäviltä tapahtumilta tai päivityksiltä ennen julkaisua.
- Kun olet valmis suorittamaan hyväksyntätestauksen tai julkaisun harjoituksen, päivitä eristysympäristö tuotantoympäristöstä. Lisätietoja on kohdassa [Esiintymän kopioiminen](hr-admin-setup-copy-instance.md).
- Testaa kaikki käyttöönottosuunnitelman vaiheet eristysympäristöissä ja vahvista sen jälkeen eristysympäristö suorittamalla pistetarkistuksia tai suorittamalla hyväksyntätestauskomentosarjoja ympäristössä.
  - Testeihin tulisi kuulua kaikki tietojen siirrot mukaan lukien julkaisussa tarvittavat muunnokset.
  - Prosessin tulisi sisältää kaikkien vanhojen järjestelmien käytöstäpoiston harjoitus.
  - Varmista, että sisällytät kaikki integroinnin käyttöönoton vaiheet tai ulkoisen järjestelmän vaiheet käyttöönoton harjoituksessa.
- Jos käyttöönoton harjoituksen aikana löytyy ongelmia, voi olla tarpeen toinen käyttöönoton harjoitus. Tämän vuoksi suosittelemme, että suunnittelet projektisuunnitelmaan kaksi käyttöönoton harjoitusta.

## <a name="fasttrack-go-live-assessment"></a>FastTrackin julkaisuarviointi

FastTrack-asiakkaat, joilla on FastTrack-ratkaisuarkkitehdin tuki, suorittavat julkaisuarvioinnin Microsoft FastTrackin kanssa. Lisätietoja on kohdassa  [Microsoft FastTrack](/dynamics365/fasttrack/). 

FastTrack-tiimi pyytää täyttämään noin kahdeksan viikkoa ennen julkaisua [julkaisun tarkistusluettelon](https://go.microsoft.com/fwlink/?linkid=2146013).

Projektipäällikön tai keskeisen projektiryhmän jäsenen on täytettävä julkaisun tarkistusluettelo projektin julkaisua edeltävässä vaiheessa. Yleensä tarkistusluettelo täytetään 4–6 viikkoa ennen ehdotettu julkaisupäivää sen jälkeen, kun käyttäjän hyväksyntätestaus on valmistunut tai melkein valmis. 

Täytetty julkaisun tarkistusluettelo lähetetään sähköpostitse FastTrack-ratkaisuarkkitehdille. Sähköpostin vastaanottajina on oltava aina myös asiakkaan ja toteutuskumppanin keskeinen sidosryhmä. 

Kun tarkistusluettelo on lähetetty, FastTrack-ratkaisuarkkitehti perehtyy projektiin ja tekee arvioinnin, jossa käsitellään projektin julkaisun onnistumiseen liittyviä mahdollisia riskejä, parhaita käytäntöjä ja suosituksia. Joissakin tapauksissa ratkaisuarkkitehti voi nostaa esille riskitekijöitä ja pyytää suunnitelman niiden korjaamiseksi. 

## <a name="see-also"></a>Lisätietoja

[Käyttöönoton usein kysytyt kysymykset](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

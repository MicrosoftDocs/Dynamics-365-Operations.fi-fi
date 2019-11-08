---
title: Attractin LinkedIn-integraation usein kysytyt kysymykset
description: Tässä ohjeaiheessa on vastauksia LinkedInin ja Microsoft Dynamics 365 Talent – Attractin integraatiota koskeviin kysymyksiin.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: b77ad598ba209dbbd73765c49947e84a3995153d
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550364"
---
# <a name="attract-integration-with-linkedin-faq"></a>Attractin LinkedIn-integraation usein kysytyt kysymykset

[!include [banner](includes/banner.md)]

LinkedIn on maailman suurin verkossa toimiva asiantuntijaverkosto. Microsoft Dynamics Talent: Attractin ja LinkedInin integroinnin avulla saat käyttöösi koko maailman parhaat osaajat. Attractissa on mahdollista julkaista työpaikkoja suoraan LinkedIniin. Lisäksi ehdokkaan tiedot voidaan hakea LinkedInistä Attractiin.

## <a name="for-recruiters-and-hiring-managers"></a>Työhönottajat ja työhön ottavat esimiehet

Nämä vastaukset koskevat usein kysyttyjä kysymyksiä siitä, miten Attractia ja LinkedIniä käytetään yhdessä.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Mitä LinkedIn-toimintoja saan käyttööni Attractilla?

Kun Attract on integrointi LinkedIniin, voit suorittaa seuraavat tehtävät:

- [Työpaikkojen julkaiseminen LinkedInissä](./attract-post-jobs-to-linkedin.md) (maksuttomina rajoitettuina listauksina).
- [Ehdokkaan tietojen vienti LinkedInistä Attractiin](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Ehdokkaat voivat hakea työpaikkoja LinkedInissä](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Mitä tarvitsen, ennen kuin voi julkaista työpaikkoja LinkedInissä?

Järjestelmänvalvojan on [määritettävä LinkedIn-integraatio Attractissa](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Sen jälkeen, voit aloittaa käytön.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Miten työpaikkoja julkaistaan LinkedIniin Attractista?

Sen jälkeen kun olet luonut työpaikan Attractissa, sinun tarvitsee vain valita LinkedInin **Julkaise nyt** -painike. Lisätietoja on kohdassa [Työpaikkojen julkaiseminen LinkedIniin Attractista](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Saanko ehdokkaan tiedot LinkedInistä Attractiin?

Kyllä. Jos näet LinkedInissä hyvän ehdokkaan, ehdokkaan tiedot on helppo tuoda Attractiin. Lisätietoja on kohdassa [Ehdokkaiden rekrytointi LinkedIn Recruiterin avulla](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Miten saan apua LinkedInin käyttämiseen Attractista?

Jos kirjautumisessa tai työpaikkojen julkaisemisessa LinkedIniin Attractista on ongelmia, katso kohta [LinkedIn-integraation vianmääritys](./attract-troubleshoot-linkedin.md).

Jos kyse on jostain muusta Attractin ongelmasta, katso [Talent-tuen saaminen](./talent-support.md). Jos tarvitset LinkedIn-tukea, katso [LinkedInin tukisivu](https://www.linkedin.com/help).

## <a name="for-admins-and-developers"></a>Järjestelmänvalvojat ja kehittäjät

Nämä vastaukset koskevat usein kysyttyjä kysymyksiä Attractin ja LinkedInin integraation määrittämisestä.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Miten Attract määritetään siten, että työhönottajat ja työhön ottavat esimiehet voivat julkaista työpaikkoja LinkedInissä?

Voit määrittää asetuksia hallintakeskuksen **LinkedIn-integrointi**-välilehdessä. Lisätietoja on kohdassa [LinkedIn-integraation määrittäminen](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>Voiko ehdokkaan tietoja viedä LinkedInistä?

Kyllä, mutta LinkedIn Recruiter -integraatio on määritettävä ensin. Lisätietoja on kohdassa [LinkedIn-integraation määrittäminen](./attract-admin-linkedin.md).

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>Miten voin julkaista työpaikkoja LinkedInin Premium-työpaikoissa?

Vaikka Attract on tehokas ratkaisu työpaikkojen julkaisemiseen LinkedInissä, joskus on voitava toimia joustavammin. Haluat ehkä esimerkiksi julkaista Premium-työpaikkoja maksuttomien rajoitettujen listauksien lisäksi. Tai sitten ehkä haluat, että LinkedIn käsittelee erätyöjulkaisut useita kertoja päivässä.

#### <a name="types-of-linkedin-job-posts"></a>LinkedIn-työpaikkojen julkaisutyypit

LinkedInissa on seuraavan tyyppisiä työpaikkajulkaisuja:

- **Rajoitettu listaus** – Nämä maksuttomat työpaikkajulkaisut näkyvät hakutuloksissa, kun ehdokkaat etsivät työpaikkoja LinkedInissä ja yrityksen LinkedIn-sivulla. Rajoitettujen listausten kohteena on aktiiviset työnhakijat. Attract toimittaa tällaisen luettelotyypin LinkedIniin. Rajoitetun listauksen työpaikkoja ei voi mainostaa LinkedInissä. Jos haluat mainostaa rajoitettuja listauksia, sinun on otettava työpaikkojen paketointi käyttöön yhteistyössä LinkedInin kanssa. Lisätietoja työpaikkojen paketoinnista on kohdissa [Rajoitettujen listauksien vertailu työpaikkojen paketoinnin Premium-työpaikkoihin](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) ja [Usein kysyttyjä kysymyksiä työpaikan paketointi plus -palvelusta](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **Premium-työpaikat** – Nämä ostetut julkaisut näkyvät LinkedInissä useissa eri paikoissa, kuten LinkedInin syötteessä, sähköposteissa ja **mahdollisesti kiinnostavissa työpaikoissa**. Vaikka Premium-työpaikkojen kohteena on passiiviset ehdokkaat, ne näkyvät myös työpaikkahauissa.

Attract julkaisee työpaikat LinkedInissä rajoitettuina listauksina. Jos haluat käyttää Premium-työpaikkoja, sinun on käytettävä LinkedIn Recruiterin työpaikkojen paketointia. Työpaikkojen paketointia varten LinkedInin kanssa on tehtävä työpaikkojen paketointisopimus. Lisätietoja on kohdassa [Työpaikkojen paketointi LinkedIn Recruiterissa – yleiskatsaus](https://www.linkedin.com/help/recruiter/answer/79037).

#### <a name="frequency-of-batch-processing-on-linkedin"></a>Eräprosessien toistoväli LinkedInissä

LinkedIn käsittelee työpaikkajulkaisut erinä Attractin kautta kerran päivässä. Tämän vuoksi voi kestää jopa 48 tuntia, ennen kuin työpaikat näkyvät LinkedInissä sen jälkeen, kun ne julkaistu Attractin kautta. Jos työpaikkojen on tultava nopeammin näkyviin LinkedIniin tai jos haluat toimia joustavammin, voit käyttää Recruiter System Connect -sovelluksen ohjelmointirajapintaa LinkedInistä. Lisätietoja on kohdassa [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect).

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>Taulukko työpaikkojen julkaisuvaihtoehdoista LinkedInissä

Seuraavassa taulukossa esitellään eri vaihtoehdot, jolla työpaikkoja voi julkaista LinkedInissä. Siinä ilmoitetaan kunkin vaihtoehdon edut sekä annetaan lisätietoja.

|  | Kerätä | Työn paketointi LinkedIn Recruiterissa | Recruiter System Connect -ohjelmointirajapinta |
|---|---|---|---|
| **Kuvaus** | Attract julkaisee työpaikat LinkedInissä XML-syötteenä. | Yritys tekee sopimuksen LinkedInin kanssa ja toimittaa XML-syötteen työpaikkojen julkaisua varten. | Asiakas synkronoi tiedot Attractin ja LinkedIn Recruiterin välillä ohjelmointirajapinnan avulla. |
| **Minkä tyyppisiä työpaikkoja voin julkaista?** | Rajoitettu listaus | Premium-työpaikka tai rajoitettu listaus | Rajoitettu listaus |
| **Voinko mainostaa työtä LinkedInissä?** | Ei | Premium-työpaikat: Kyllä<br>Rajoitetut listaukset: ei | Ei |
| **Kuinka usein LinkedIn julkaisee työpaikat?** | Kerran päivässä | Kerran päivässä | Useita kertoja päivässä ohjelmointirajapinnan määrittämällä tavalla |
| **Onko LinkedInin suosittelema?** | Ei | Kyllä | Ei |
| **Mitä tarvitsen?** | Attractin osto | Työpaikkojen paketointisopimus LinkedInin ja Premium-työpaikkojen osto | Ohjelmointirajapintasopimus LinkedInin kanssa | 
| **Mistä lisätietoja voi etsiä?** | [LinkedIn-integraation määrittäminen](./attract-admin-linkedin.md) | [Työpaikkojen paketointi LinkedIn Recruiterissa – yleiskatsaus](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> LinkedIn Recruiter System Connect -käyttöoikeutta ei tarvita työpaikkojen julkaisemiseen LinkedIniin Attractista.

## <a name="see-also"></a>Lisätietoja

[LinkedIn-integraation määrittäminen](./attract-admin-linkedin.md)

[Työpaikkojen julkaiseminen LinkedInissä Attractista](./attract-post-jobs-to-linkedin.md)

[Ehdokkaiden rekrytointi LinkedIn Recruiter -ratkaisulla](./attract-linkedin-recruiter.md)

[LinkedIn-integraation vianmääritys](./attract-troubleshoot-linkedin.md)

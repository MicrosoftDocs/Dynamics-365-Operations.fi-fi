---
title: Ehdokkaiden rekrytointi LinkedIn Recruiterilla Attractissa
description: Rekrytoi ehdokkaita työpaikkaan LinkedIn Recruiterin avulla käyttämällä Microsoft Dynamics 365 Talent – Attractin LinkedIn-integraatiota.
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528266"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a>Ehdokkaiden rekrytointi LinkedIn Recruiterilla Attractissa

[!include [banner](includes/banner.md)]

LinkedIn on maailman suurin verkossa toimiva asiantuntijaverkosto, jonka avulla koko maailman parhaat osaajat ovat käytettävissä. Microsoft Dynamics 365 Talent: Attractin avulla voit rekrytoida ehdokkaita suoraan LinkedInistä. Niinpä sopivien osaajien löytäminen avoimiin työpaikkoihin on helpompaa kuin koskaan. Kun olet muodostanut LinkedIn-yhteyden Attractin kautta, voit tarkastella työpaikkaan sopivia mahdollisia LinkedIn-ehdokkaita ja viedä heidät Attractiin yhdellä napsautuksella.

Jos tämä toiminto ei näytä olevan käytössä, ota yhteys järjestelmänvalvojaan. Ennen kuin LinkedIn Recruiteria voi käyttää Attractista, järjestelmänvalvojan on [LinkedIn-integraatio](./attract-admin-linkedin.md). Voit sitten määrittää LinkedIn Recruiter -yhteyden ja aloittaa ehdokkaiden etsimisen.

>[!IMPORTANT]
>1. heinäkuuta 2020 alkaen LinkedInissä ei enää ole Internet Explorer 11 -tukea. Käyttäjät voivat yhä käyttää LinkedInia Internet Explorer 11:n avulla, mutta heitä kehotetaan päivittämään selain tai käyttämään toista selainta. Lisätietoja on kohdassa [LinkedInin tuetut internet-selaimet](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>LinkedIn Recruiter -yhteyden määrittäminen

LinkedIn Recruiter -yhteys on määritettävä, ennen kuin voit aloittaa LinkedIn Recruiterin käytön Attractissa. Tarvitset tässä vaiheessa LinkedIn Recruiter -tunnistetiedot.

1. Valitse **Asetukset**-painike (rataskuvake) sivun oikeassa yläkulmassa.
2. Valitse **Käyttäjäasetukset**.
3. Valitse **Yhteydet**-välilehdessä **Yhdistä**-asetus **LinkedIn**-kohdan vieressä. Noudata LinkedInin antamia ohjeita.

    ![[LinkedIn Recruiterin yhteyden määrittäminen Attractista](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>LinkedIn-ehdokkaiden näyttäminen Attractissa

Kun olet muodostanut LinkedIn Recruiter -yhteyden, voit tarkastella ehdokkaiden LinkedIn-profiileja Attractissa.

>[!NOTE]
>Jos sinulle on määritetty työhönottajan rooli, näet ehdokkaiden kaikki tiedot.<br><br>
>Jos sinulla on työhön ottavan esimiehen rooli tai jos sinulle ei ole määritetty roolia, muista kirjautua ulos LinkedInista tai LinkedIn Recruiterista ennen kuin siirryt Attractissa ehdokkaan LinkedIn-välilehteen. Näkyvissä ovat ehdokkaan julkisen profiilin perustiedot, kuten etu- ja sukunimi.

1. Valitse Attractissa vasemmalla **Työt** tai **Kykypoolit** ja valitse sitten hakija.

    ![[LinkedIn-ehdokkaiden näyttäminen Attractissa](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. Valitse ehdokkaan profiilissa **LinkedIn**-välilehti. Voit tarkastella ehdokkaan profiilia ja InMail-historiatietoja.

   ![Ehdokkaan LinkedIn-tietojen tarkasteleminen](./media/attract-candidate-linkedin-tab.png)

Tässä voit myös tehdä seuraavia toimenpiteitä:

- Valitse **Rekrytointitehtävät**-välilehti, jos haluat tarkastella seuraavia tietoja:
   
   - Työhönottajan huomautukset (sekä julkiset että yksityiset). Oletusarvoisest huomautukset ovat yksityisiä. Ne näkyvät vain huomautusten omistajille.
   - InMail-aktiviteetti (mutta ei InMail-sisältö). Siirry sivun alaosaan, jos haluat tarkastella InMail-siirtoa ja prospektia sekä organisaation muita käyttäjiä, jotka ovat yhteydessä prospektin kanssa.
   - Ehdokkaan hylkäystehtävä

- Valitse **Lähetä InMail**, jos haluat lähettää InMailin poistumatta Attractista.

- Valitse **Tallenna työhön**, jos haluat tallentaa työn poistumatta Attractista.

> [!NOTE]
> Ehdokkaan LinkedIn-profiili näytetään Attractissa, kun ehdokkaan Attract-tiedot vastaavat LinkedIn-tietoja. Käytettävät vastaavuussäännöt:
> 
> 1. Jos sähköpostiosoite ja LinkedIn-jäsentunnus ovat samat Attractissa ja LinkedInissä, ehdokkaan profiili näytetään. Ehdokkaat voivat kuitenkin valita Attractissa, linkittävätkö he LinkedIn-profiilinsa vai eivät.
> 2. Jos sähköpostiosoite tai LinkedIn-jäsentunnus eivät vastaa toisiaan, näkyviin tulee luettelo mahdollisista ehdokkaista. Voit sitten valita ehdokkaan luettelosta ja linkittää profiilin.
> 3. Jos hyviä vastaavuuksia ei ole, saat ilmoituksen siitä, ettei vastaavuutta löytynyt.

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a>LinkedIn-ehdokkaiden vienti Attractiin yhdellä napsautuksella

Samalla kun tarkastelet ehdokkaista LinkedIn Recruiterissa, voit viedä heidät Attractissa avoimina oleviin työpaikkoihin. Tätä vaihetta varten tarvitaan Attractin työhönottajan tai työhön ottavan esimiehen käyttöoikeudet. Lisätietoja näistä Attractin rooleista kohdassa [Suojaus ja roolien hallinta Attractissa](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).

Sinun on myös varmistettava, että työpaikassa on Prospekti-vaihe. Lisätietoja on kohdassa [Prospekti-tehtävä](./activities-attract.md#prospect-activity).

1. Luo Attractissa työpaikka, määritä soveltuvat roolit ja aktivoi työpaikka.
2. Etsi LinkedIn Recruiterissa työpaikkaan hyvä ehdokas ja siirry ehdokkaan profiiliin.
3. Etsi yhteyshenkilökortin työpaikan hakuruudun avulla työpaikka nimikkeen tai Attractissa aktivoidun työpaikan tunnuksen perusteella. Jos et löydä työpaikkaa, etsi oikea Attract-esiintymä valitsemalla **Vaihda ATS**.
4. Valitse ensin työpaikka ja sitten **Vie**.
5. Avaa työ Attractissa. Viety ehdokas näkyy työpaikan **Prospekti**-välilehdessä.

## <a name="view-attract-information-in-linkedin-recruiter"></a>Attract-tietojen näyttämine LinkedIn Recruiterissa

Voit seurata LinkedIn Recruiterissa, onko ehdokas hakenut organisaatiossa muita työpaikkoja, katsoa, missä työhakemusten vaiheessa ehdokas on, ja tarkastella Attractin palautetta ja kommentteja issa.

1. Avaa LinkedIn Recruiter ja valitse ehdokkaan profiili.
2. Pidä osoitinta **ATS:n**-kohdan päällä.
3. Tarkastele ehdokkaan Attractiin tallennettuja tietoja valitsemalla jokin seuraavista vaihtoehdoista:

    - **Työpaikat ja tilat** – voit katsoa työpaikkoja, joissa ehdokas on osallisena, viimeisintä tilaa ja ehdokkaan etenemistä kussakin työpaikassa.
    - **Haastattelun palaute** – katso, mitä palautetta haastattelijat ovat lähettäneet Attractissa.
    - **Huomautukset** – katso, mitä tätä ehdokasta koskevia huomautuksia on annettu Attractissa.

    ![[Attract-tietojen tarkastelemien LinkedIn Recruiterissa](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> Ehdokkaan ja hakemuksen tietoja ei synkronoida LinkedIn Recruiterin kanssa, jos ehdokas ei ole siirtynyt prospektivaiheesta eteenpäin.

## <a name="view-linkedin-talent-pools"></a>LinkedInin kykypoolien näyttäminen

Jos ehdokkaat hyväksyvät LinkedIn-profiiliinsa jakamisen organisaation käyttäjien kanssa, Attractiin luodaan uusi ehdokastietue. Nämä ehdokkaat näkyvät sitten järjestelmän luomassa LinkedInin kykypoolissa.

1. Valitse Attractissa vasemmalla **Kykypoolit**.
2. Valitse LinkedInin kykypooli Näet luettelon ehdokkaista ja heidän LinkedInistä saadut tynkäprofiilit. Tynkäprofiilit sisältävät ehdokkaan etu- ja sukunimen sekä sähköpostiosoitteen, jos ehdokas on valinnut sen jakamisen.

## <a name="see-also"></a>Lisätietoja

[Attractin LinkedIn-integraation usein kysytyt kysymykset](./attract-linkedin-faq.md)

[Microsoft Dynamics 365 Talent – Attractin LinkedIn-integraation määrittäminen](./attract-admin-linkedin.md)

[Työpaikkojen luominen, hyväksyminen ja julkaiseminen Attractissa](./creating-jobs-attract.md)

[Työpaikkojen julkaiseminen LinkedInissä Microsoft Dynamics 365 Talent – Attractista](./attract-post-jobs-to-linkedin.md)

[LinkedInin ja Microsoft Dynamics 365 Talent – Attractin integroinnin vianmääritys](./attract-troubleshoot-linkedin.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
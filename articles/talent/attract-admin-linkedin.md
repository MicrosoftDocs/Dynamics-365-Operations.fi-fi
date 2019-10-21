---
title: Microsoft Dynamics 365 Talent – Attractin LinkedIn-integraation määrittäminen
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent – Attractin LinkedIn-integraation määrittämistä siten, että työpaikkoja on helppo julkaista LinkedIniin Attractista ja että työhönottajat voivat synkronoida työhönottotiedot ehdokkaan LinkedIn-profiilin kanssa.
author: andreabichsel
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
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 6b86cafdf364f2de051f3d8ceab7413c2c13c3a5
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009966"
---
# <a name="set-up-linkedin-integration"></a>LinkedIn-integraation määrittäminen

[!include[banner](../includes/banner.md)]

Auta työnottajia ja työhön ottavia esimiehiä rekrytoimaan parhaita osaajia määrittämällä LinkedInin integraatio Microsoft Dynamics 365 Talent: Attractin kanssa. Attractin avulla voit julkaista työpaikkoja suoraan maailman suurimpaan verkossa toimivaan asiantuntijaverkostoon, LinkedIniin.

Attractista LinkedIniin julkaistavat työpaikat ovat rajoitetun listauksen työpaikkoja, jotka yritys voi julkaista ilman lisäkustannuksia. Näitä listauksia voi käyttää vain LinkedIn-ohjelmistokumppaneiden, kuten Attractin, kautta. Ne eivät näy yrityksen LinkedIn-sivun **Urat**-paneelissa, koska vain maksetut ilmoitukset näkyvät siellä. Ne kuitenkin näkyvät, kun mahdolliset ehdokkaat tarkastelevat kaikkia vapaita työpaikkoja. Rajoitetut listaukset näkyvät myös LinkedInin työpaikkojen hauissa.

Attractissa on kaksi tapaa, jolla LinkedIn-integraatio auttaa rekrytoimiaan ehdokkaita suositusta urasivustosta:

- työpaikkojen julkaiseminen Attractista LinkedIniin
- ehdokkaiden rekrytointi LinkedInistä Attractiin.

Kumpikin vaihtoehto määritetään hallintakeskuksen **LinkedIn-integrointi**-välilehdessä. Avaa hallintakeskus siirtymällä osoitteeseen <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> LinkedIn Recruiter -integraation käyttöä varten Attractissa tarvitaan [kattava työhönottolaajennuksen](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) ja [LinkedIn Recruiterin käyttöoikeudet](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Lisätietoja on kohdassa [Mikä Attractin versio?](./attract-comprehensive-hiring.md).

Jos työpaikkojen julkaisemisessa LinkedIniin on ongelmia, katso kohta [LinkedIn-integraation vianmääritys](./attract-troubleshoot-linkedin.md).

Lisätietoja muista työpaikkojen julkaisutavoista LinkedInissä on kohdassa [LinkedInin usein kysytyt kysymykset](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>LinkedIn-työpaikkailmoituksen määrittäminen

Ennen kuin työpaikkoja voi julkaista Attractista LinkedIniin, tarvitset [LinkedIn-yritystunnuksen](https://aka.ms/findID). LinkedIn-yritystunnus on numerojono, jolla yritys tunnistetaan yksilöivästi LinkedInissä. Lisätietoja on kohdassa [LinkedIn-yritystunnuksen liittäminen LinkedIn-työpaikkailmoitussivulle – usein kysyttyjä kysymyksiä](https://aka.ms/findID).

Attract lähettää työpaikkailmoitussyötteen LinkedIniin ja LinkedIn tarkistaa syötteen noin kerran päivässä. Työpaikkojen julkaiseminen sivustossa voi kestää jopa 48 tuntia.

LinkedIniin julkaistut työpaikat näkyvät julkaistuna LinkedIn-sivustossa. LinkedInissä ei ole työpaikkojen julkaisun testiympäristöä. Varmista tämän vuoksi, ettet vahingossa julkaise testityöpaikkoja. 

1. Valitse **Asetukset**-valikossa (hammasrataskuvake) oikeassa alakulmassa **Hallintakeskus**. Vaihtoehtoisesti voit siirtyä sivulle <https://attract.talent.dynamics.com/adminsettings>.
2. Valitse **LinkedIn-integraatio**-välilehti.
3. Anna **Yrityksen nimi** -kohdassa yrityksen nimi ja **Yritystunnus**-kohdassa LinkedIn-yritystunnus. Varmista, että yrityksen nimi vastaa yrityksen LinkedIn-sivulla näkyvää nimeä. Lisätietoja LinkedIn-yritystunnuksista on kohdassa [LinkedIn-yritystunnuksen liittäminen LinkedIn-työpaikkailmoitussivulle – usein kysyttyjä kysymyksiä](https://www.linkedin.com/help/linkedin/answer/98972).

    Jos organisaation tietoja on muutettava, lisätietoja on kohdassa [Organisaation osoitteen, teknisen yhteyshenkilön ja muiden tietojen muuttaminen](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Jos ongelmia on edelleen, ota yhteys [LinkedIn-tukeen](https://www.linkedin.com/help/linkedin).

4. Valitse **Tallenna**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>LinkedIn Recruiterin määrittäminen Attractin kanssa 

Jos haluat, että työhönottajat voivat rekrytoida työntekijöitä LinkedIn Recruiterissa, LinkedIn Recruiter -integraatio on määritettävä Attractissa. Määritysprosessin suorittamista varten on tehtävät yhteistyötä sen käyttäjän kanssa, joka on organisaation LinkedIn Recruiter -sopimuksen järjestelmänvalvoja.

1. Valitse **Asetukset**-valikossa (hammasrataskuvake) oikeassa alakulmassa **Hallintakeskus**. Vaihtoehtoisesti voit siirtyä sivulle <https://attract.talent.dynamics.com/adminsettings>.
2. Valitse **LinkedIn-integraatio**-välilehti.

    [![LinkedIn Recruiter -integroinnin aloittaminen Attractin hallintanäkymässä](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Aloita määrittäminen valitsemalla **Muodosta yhteys**. Sinut opastetaan LinkedIn-kirjautumisprosessin läpi.
4. Jos käytössä on paikkoja useissa LinkedIn-sopimuksissa, valitse sopimus, jonka haluat yhdistää Attract-järjestelmään. Jos käytössä on paikka vain yhdessä LinkedIn-sopimuksessa, voit ohittaa tämän vaiheen.
5. Valitse **Recruiter System Connect (RSC)** -kohdassa **Pyyntö**.

    [![LinkedIn Recruiter -integroinnin pyytäminen Attractin hallintanäkymässä](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. **Recruiter System Connect (RSC)** -asetuksena pitäisi nyt olla **Kumppanivalmius**. Jos sivulla näkyy ilmoitus, jossa pyydetään **ilmoittamaan kumppanille**, odota muutama sekunti, valitse sitten **kumppanille ilmoittaminen** ja päivitä sivu. Asetuksena pitäisi nyt olla **kumppanivalmius**.

    [![Attractin hallintanäkymä ilmaisee, että Attractin pyynnöt on tehty](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Seuraavien vaiheiden suorittamista varten tarvitaan LinkedIn Recruiter -sopimuksen järjestelmänvalvojan oikeudet.

    1. Kirjaudu LinkedIniin käyttämällä järjestelmänvalvojatiliä ja valitse sitten oikeassa yläkulmassa **LinkedIn Recruiter**. 
    2. Valitse sivun yläosan **Lisää**-valikossa **Järjestelmänvalvojan asetukset** ja valitse sitten **ATS**-välilehti.
    3. Ota yhden sopimuksen vienti käyttöön yhdellä napsautuksella valitsemalla **sopimustason käyttöoikeus (tämän sopimuksen jokaiselle käyttäjälle)**. Voit ottaa toiminnon käyttöön koko yrityksessä valitsemalla **yritystason käyttöoikeudet käyttöön (jokaisessa yrityksen sopimuksessa)**.

    [![Attract-integroinnin käyttöönotto LinkedIn Recruiterin hallintanäkymässä](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Valitse Attractin hallintakeskuksessa **LinkedIn-integraatio**-välilehti. **Recruiter System Connect (RSC)** -asetuksena pitäisi olla nyt **Käytössä**.

    [![LinkedIn Recruiterin integrointi valmis](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Hae LinkedInin kautta -toiminnon määrittäminen Attractissa

Voit antaa ehdokkaiden hakea työpaikkoja LinkedIn-profiilien avulla. Lisätietoja Hae LinkedInin kautta -toiminnosta on kohdassa [LinkedInin monipuolinen käyttö: Hae LinkedInin kautta -toiminto](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Tämä ominaisuus on tällä hetkellä vain esiversiossa. Varmista ennen näiden vaiheiden suorittamista, että Hae LinkedInin kautta -toiminto on otettu käyttöön. Lisätietoja esiversiotoimintojen käyttöönottamisesta on kohdassa [Esiversiotoimintojen käyttö Talentissa](./access-preview-feature.md).

1. Valitse **Asetukset**-valikossa (hammasrataskuvake) oikeassa alakulmassa **Hallintakeskus**. Vaihtoehtoisesti voit siirtyä sivulle <https://attract.talent.dynamics.com/adminsettings>.
2. Valitse **LinkedIn-integraatio**-välilehti.

    [![LinkedIn Recruiter -integroinnin aloittaminen Attractin hallintanäkymässä](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Aloita määritys valitsemalla **Hae LinkedInin kautta** -kohdan vieressä **Muodosta yhteys**. Sinut opastetaan tämän LinkedIn-prosessin läpi.

## <a name="see-also"></a>Lisätietoja

[LinkedInin usein kysytyt kysymykset](./attract-linkedin-faq.md)

[Työpaikkojen julkaiseminen ulkoisille sivustoille Attractista](./posting-jobs-external.md)

[Ehdokkaiden rekrytointi LinkedIn Recruiter -ratkaisulla](./attract-linkedin-recruiter.md)

[Työpaikkojen luominen](./creating-jobs-attract.md)

[LinkedIn-integraation vianmääritys](./attract-troubleshoot-linkedin.md)

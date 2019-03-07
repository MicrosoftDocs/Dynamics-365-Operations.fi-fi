---
title: LinkedIn Recruiterin käyttö hankinnassa
description: Tässä ohjeaiheessa käsitellään koneoppimisen käyttöä työpaikkojen ja niiden ehdokassuositusten hankkimisessa.
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 9bb323728923ff3b09ff0bfba3849f3c5d84eb34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304159"
---
# <a name="sourcing-with-linkedin-recruiter"></a>LinkedIn Recruiterin käyttö hankinnassa
[!include[banner](../includes/banner.md)]

LinkedIn on maailman suurin kykytietokanta. Se on myös usein ensisijainen järjestelmä, jonka avulla työhönottajat etsivät ehdokkaita, viestivät heidän kanssaan ja hankkivat ehdokkaita työpaikkoihin, joihin työhönottajat etsivät työntekijää. LinkedIn Recruiterin ja Dynamics 365 for Talent: Attractin välinen integraatio helpottaa työhönottoa ja tietojen pitämistä synkronoituna kahden järjestelmän välillä.

> [!NOTE]
> LinkedIn Recruiterin ja Attractin väliseen integraatioon tarvitaan kattavan työhönottolaajennuksen ja LinkedIn Recruiterin käyttöoikeudet.

## <a name="set-up-linkedin-recruiter-with-attract"></a>LinkedIn Recruiterin ja Attractin yhteiskäytön määrittäminen 

LinkedIn Recruiter -toimintojen käyttö edellyttää, että Attract-esiintymään on määritetty sopimus- tai yritystasoiset käyttöoikeudet. Määritysprosessin suorittamista varten on tehtävät yhteistyötä sen käyttäjän kanssa, joka on LinkedIn Recruiter -sopimuksen järjestelmänvalvoja. Määritä LinkedIn Recruiterin ja Attractin yhteiskäyttö seuraavien ohjeiden mukaisesti.

1.  Kirjaudu Attractiin järjestelmänvalvoja ja valitse **Järjestelmänvalvojan asetukset**.

2.  Valitse vasemmassa ruudussa **LinkedIn-integrointi**-välilehti.

[![LinkedIn Recruiter -integroinnin aloittaminen Attractin hallintanäkymässä](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Aloita asennus valitsemalla **Muodosta yhteys**. Noudata opastettua LinkedIn-kirjautumista.

4.  Jos käytössä on paikkoja useissa LinkedIn-sopimuksissa, valitse sopimus, jonka haluat yhdistää Attract-järjestelmään. Jos käytössä on paikka vain yhdessä LinkedIn-sopimuksessa, tämä vaihe on tarpeeton.

5.  LinkedIn-pienoisohjelma latautuu nyt järjestelmänvalvojan asetuksiin, ja siinä on kuvassa näkyvät integraatiot. Valitse **Recruiter System Connect** -kohdassa **Pyyntö**.

[![LinkedIn Recruiter -integrointipyyntö Attractin hallintanäkymässä](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Kun integrointia on pyydetty Attractista, näkyviin tulee, että **kumppani on valmis** ja että integrointi voidaan ottaa käyttöön **Recruiterin järjestelmänvalvojan asetuksissa**. Jos sivulla näkyy ilmoitus, jossa pyydetään **ilmoittamaan kumppanille**, odota muutama sekunti, valitse sitten **kumppanille ilmoittaminen** ja päivitä sivu. Näkyvissä pitäisi nyt olla, että **kumppani on valmis**.

[![Attractin hallintanäkymä ilmaisee, että Attractin pyynnöt on tehty](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Seuraavaa vaihetta varten tarvitaan LinkedIn Recruiter -sopimuksen järjestelmänvalvojan oikeudet.

7.  Kirjaudu LinkedIniin järjestelmänvalvojan tilillä ja valitse oikeassa yläkulmassa LinkedIn Recruiter. 

8. Valitse näytön yläosan **Lisää**-valikossa **Järjestelmänvalvojan asetukset** ja valitse sitten **ATS**-välilehti.

Attract-järjestelmä on näkyvissä muutaman muun käyttöönotettavan vaihtoehdon ohella.

9. Jos haluat ottaa käyttöön vain yhden napsautuksen viennin **ATS:n ilmaisin**- tai **ATS:n profiilin pienoisohjelma** -kohdassa, valitse **Yritystason käyttöoikeus**. Jos haluat ottaa käyttöön kaikki yritystason käyttöoikeudet sekä InMail-historiatietojen, huomautusten historiatietojen ja InMailin tynkäprofiilin käyttöoikeudet, valitse **Sopimustason käyttöoikeus**.

10. Ota valittu käyttöoikeustaso käyttöön LinkedIn Recruiterin **Järjestelmänvalvoja-ATS**-setuksissa.

[![Attract-integroinnin käyttöönotto LinkedIn Recruiterin hallintanäkymässä](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Palaa Attractin järjestelmänvalvojan asetuksiin Attractin järjestelmänvalvojana ja valitse **LinkedIn-integrointi**-välilehti. LinkedIn-pienoisohjelmalataus pitäisi nyt näkyä siten, että **Käytössä**-tilassa on valittu käyttöoikeustaso käyttöönotettuna.

[![Valmis LinkedIn Recruiter -integrointi](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>LinkedIn Recruiterin toimintojen käyttäminen

Kun Attractin järjestelmänvalvoja on ottanut LinkedIn Recruiterin toiminnot käyttöön, työhön ottavat esimiehet ja työhönottajat voivat käyttää sitä. Voit ottaa nämä toiminnot käyttöön, muodostamalla yhteyden LinkedIn-tiliin **käyttäjäasetuksissa**. Sen jälkeen kun sekä järjestelmänvalvojan että käyttäjän asetukset on yhdistetty, käytössä on useita toimintoja.

### <a name="in-ats-profile-widget"></a>ATS:n profiilin pienoisohjelma

Voit tarkastella ehdokkaan LinkedIn-profiilia Attractissa. LinkedIn-pienoisohjelma näyttää hakijan profiilin, kun ATS-tiedot vastaavat käyttäjien LinkedIn-tietoja.

Voit tarkastella profiilia valitsemalla profiilin joko työstä tai kykypoolista. Valitse ehdokkaan profiilissa **LinkedIn**-välilehti, jolloin pienoisohjelma latautuu. Voit myös tallentaa ehdokkaan tällä sivulla LinkedIn Recruiter -projekteihin.
1. Jos LinkedIn löysi vastineen sähköpostin ja LinkedInin jäsentunnuksen perusteella (tarkka vastine), ehdokkaan profiili näytetään. Käyttäjällä on edelleen mahdollisuus linkittää profiili tai poistaa profiilin linkitys.

2. Jos LinkedIn ei löydä ehdokasta sähköpostiosoitteen tai jäsentunnuksen perusteella, se näyttää luettelon mahdollisista ehdokkaista ehdokkaan nimen perusteella. Käyttäjä voi sitten valita heistä yhden ja linkittää profiilin.  

3. Jos LinkedIn ei löydä yhtään hakijaa nimen perusteella, se ilmoittaa, että yhtään vastinetta ei löytynyt.

### <a name="1-click-export"></a>Yhden napsautuksen vienti 

Kun ehdokkaita haetaan LinkedInissä, voit viedä ehdokkaan yhdellä napsautuksella avoimiin työpaikkoihin. Tee vienti yhdellä napsautuksella seuraavien ohjeiden mukaisesti. Varmista ennen näiden vaiheiden suorittamista, että sinulle on määritetty työpaikan työhön ottavan esimiehen tai työhönottajan rooli ja että työpaikassa on **Potentiaalinen ehdokas** -vaihe.

1.  Luo työpaikka, määritä soveltuvat roolit ja aktivoi työpaikka.

2.  Kun työpaikka on aktivoitu, siirry LinkedIn Recruiteriin.

3.  Etsi sopiva ehdokas ja siirry tämän profiiliin.

4.  Etsi yhteyshenkilökortin työpaikan hakuruudun avulla työpaikka nimikkeen tai Attractissa aktivoidun työpaikan tunnuksen perusteella. Jos et löydä työpaikkaa, etsi oikea Attract-esiintymä valitsemalla **Vaihda ATS**.

5. Kun työpaikka on valittu, valitse **Vie**. Attract noutaa nyt ehdokkaan.

6.  Siirry Attractiin ja avaa vastaava työpaikka. Juuri viety ehdokas löytyy nyt työpaikan **Potentiaalinen ehdokas** -vaiheesta.

### <a name="in-ats-indicator"></a>ATS:n ilmaisin 

Voit seurata LinkedIn Recruiterin avulla, onko ehdokas hakenut organisaatiossa muita työpaikkoja, tarkastella, missä työhakemusten vaiheessa ehdokas on, sekä tarkastella Attractin palautetta ja kommentteja LinkedIn Recruiterissa.

1.  Avaa LinkedIn Recruiter ja etsi ehdokasprofiili.

2.  Selaa hakijan profiilissa **ATS:ssä**-osaan.

3.  Voit tarkastella pienoisohjelmalla kaikki ehdokkaan Attractissa olevia tietoja LinkedIn Recruiter -näkymässä.

4.  Valitse **Työpaikat ja tilat** -välilehti, jos haluat nähdä ehdokkaaseen liittyvät työpaikat, viimeisimmät tilat ja siirtymisen kussakin työpaikassa.

5.  Valitse **Haastattelun palaute** -välilehti, jos haluat nähdä palautteen, jonka haastattelijat ovat lähettäneet Attractissa.

6.  Valitse **Huomautukset**-välilehti, jos haluat nähdä kyseisestä hakijasta Attractissa olevat muistiinpanot.

> [!NOTE]
> Ehdokkaan ja hakemuksen tietoja ei synkronoida LinkedIn Recruiteriin, jos ehdokas ei ole siirtynyt prospektivaiheesta eteenpäin.

### <a name="inmail-history"></a>InMailin historiatiedot

LinkedInin InMailin historiatiedot ovat käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet. Kun vaihtoehto on otettu käyttöön, voit tarkastella koko ehdokkaaseen liittyviä InMailin historiatietoja. Voit tarkastella myös, kenellä muulla organisaatiossa on InMail-viestintää ehdokkaan kanssa. Et kuitenkaan voi tarkastella itse viestejä.

Voit tarkastella InMail-historiatietoja valitsemalla ehdokkaan profiilissa **LinkedIn**-välilehden ja selaamalla sivun alareunaan tarkastelemaan historiatietoja. Voit tarkastella InMail-historiatietoja, jos olet käynyt keskustelun ehdokkaan kanssa. InMail-viestit synkronoidaan Attractin kanssa parin tunnin välein.

### <a name="notes-history"></a>Huomautusten historiatiedot 

LinkedInin huomautusten historiatiedot ovat käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet. Kun tämä vaihtoehto on otettu käyttöön, voit tarkastella organisaation työhönottajien ehdokkaasta tekemiä huomautuksia.

Voit tarkastella huomautusten historiatietoja valitsemalla ehdokkaan profiilissa **LinkedIn**-välilehden ja selaamalla sivun alareunaan tarkastelemaan historiatietoja. Voit tarkastella kaikkia ehdokasta koskevia huomautuksia LinkedIn Recruiterista.

### <a name="inmail-stub-profile"></a>InMailin tynkäprofiili

InMailin tynkäprofiili on käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet. Jos ehdokkaat suostuvat jakamaan LinkedIn-profiilin kaikkien organisaation käyttäjien kanssa, voit seurata ehdokkaita Attractissa ja kullekin ehdokkaalle luodaan uusi ehdokastietue. Voit tarkastella ehdokkaan sähköpostiosoitetta, jos ehdokkaalla on jo järjestelmässä sähköpostiosoite tai jos hän on jakanut osoitteensa työhönottajan kanssa.

Voit tarkastella ehdokasluetteloa valitsemalla **Kykypoolit**. Näkyvissä on nyt järjestelmän luoma LinkedIn-kykypooli. Kykypoolissa on luettelo ehdokkaista ja heidän LinkedInista vastaanotetut tynkäprofiilit, joissa näkyy ehdokkaan etu- ja sukunimi. Ehdokkaan sähköpostitunnus on näkyvissä, jos ehdokas on valinnat sähköpostiosoitteen jakamisen.

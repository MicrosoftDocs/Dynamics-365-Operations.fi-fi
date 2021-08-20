---
title: Aseta keräilyt
description: Tässä artikkelissa kerrotaan, miten kokoelmatoiminnot määritetään.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2e06da265271e2148804c51abc7cd9ffc29a3e20e73dda3a1a23966f0e6586e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769815"
---
# <a name="set-up-collections"></a>Aseta keräilyt

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten kokoelmatoiminnot määritetään. Sinun on suoritettava joitakin määritysvaiheita, kun käytät kokoelmat-ominaisuutta. Käytettävissä on myös valinnaisia ominaisuuksia, kuten asiakaspooleja ja kokoelmaryhmiä. 

- Erääntymiskausien määritykset
- Erääntymistilannevedokset
- Kirjauskansioiden nimet
- Poistotapahtuman syykoodi
- Perimisasiamiehet
- Poistotili
- NSF (Ei katetta) -tiedot
- Outlook-asetusten määrittäminen **Perintä**-sivun käyttäjille
- Sähköpostiosoitteet

Näitä kohtia käsitellään tarkemmin koko tämän aiheen loppuosassa. 

## <a name="set-up-aging-period-definitions"></a>Määritä erääntymiskausimääritykset

Määritä erääntymiskausimääritys. Erääntymiskausimääritys määrittää sarakkeet, jotka näkyvät **Erääntyneet saldot**-, **Perintätehtävät**- ja **Perintätapaukset**-luettelosivuilla. Se määrittää myös kaudet, jotka näkyvät **Perintä**-sivulla. Jos asiakaspooli on määritetty, käytetään poolin erääntymiskausimääritystä. Jos poolia ei ole määritetty, käytetään oletuserääntymiskausimääritystä, joka on määritetty **Myyntireskontran parametrit** -sivulla. Jos oletuserääntymiskauden määritystä ei ole määritetty, käytetään **Erääntymiskausien määritykset** -sivun ensimmäistä erääntymiskausimääritystä.

## <a name="create-an-aging-snapshot"></a>Erääntymistilannevedoksen luominen
Luo erääntymistilannevedostietueet kaikkia asiakkaita tai asiakaspoolin asiakkaita varten. Erääntymistilannevedostiedot näkyvät **Erääntyneet saldot** -luettelosivulla ja **Perintä**-sivulla. Erääntymistilannevedos on luotava, ennen kuin luettelosivua voi käyttää. Luettelosivulla näkyvät vain niiden asiakkaiden tiedot, joita varten on luotu erääntymistilannevedos.

## <a name="optional-set-up-customer-pools"></a>Valinnainen: Asiakaspoolien määrittäminen
Voit määrittää asiakaspoolit, jotka edustavat asiakasryhmiä. Voit käyttää asiakaspooleja **Perintä**-luettelosivuilla näkyvien asiakastietojen suodattimina **Perintä**-sivulla tai luodessasi erääntymistilannevedoksia.

## <a name="optional-create-a-collections-team"></a>Valinnainen: Perimisryhmän luominen
Jos organisaatiossasi on useita perimistyötä tekeviä henkilöitä, voit määrittää perimisryhmän. Voit valita ryhmän **Myyntireskontran parametrit** -sivulla. Jos et luo perimisryhmää, ryhmä luodaan automaattisesti, kun määrität perimisasiamiehet **Perimisasiamies**-sivulla.

## <a name="set-up-a-collections-case-category"></a>Perintätapausluokan määrittäminen
Järjestä perimistyösi tapausten avulla määrittämällä tapausluokka, jonka luokkatyyppi on **Perintä**. Tätä tarvitaan vain, jos haluat käyttää tapaustoimintoa **Perintä**-sivulla.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Kirjauskansioiden nimien määrittäminen (selvitys, poisto ja NSF)
Määritä kirjauskansioiden nimet, joita käytetään tapahtumien käsittelyyn **Perintä**-sivulla. Tämä käsittely sisältää tapahtuman tilityksen, tapahtuman poistamisen ja ei katetta -maksun käsittelyn.

| Kuvaus | Kirjauskansion tyyppi     |
|-------------|------------------|
| Tilitys  | Asiakkaan maksu |
| Poisto   | Päivittäin            |
| KATE PUUTTUU         | Asiakkaan maksu |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Poistotapahtumien syykoodin määrittäminen
Määritä oletussyykoodi, jota käytetään, kun tapahtumia kirjataan poistona **Perintä**-sivulla. Voit vaihtaa koodin poistoprosessin aikana.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Sähköpostiliitteiden kansion määrittäminen ja sähköpostimallien luominen
Jos lähetät **Perintä**-sivulta sähköpostiviestejä, joiden liitteenä on Microsoft Excel -tiedostoja, voit luoda kyseisille viesteille valinnaisia sähköpostimalleja.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Myyntireskontran parametrien määrittäminen perintää varten
Määritä **Perintä**-välilehdessä näkyvät myyntireskontran parametrit.

## <a name="optional-set-up-collections-agents"></a>Valinnainen: Perimisasiamiesten määrittäminen
Jos organisaatiossasi on useita perimistyötä tekeviä henkilöitä, voit määrittää perimisasiamiehen. Perimisasiamies on työntekijä, joka on määritetty käyttäjäksi **Käyttäjäsuhteet**-sivulla. Voit määrittää perimisasiamiehiä varten asiakaspooleja (asiakaskyselyjä), joiden avulla perimisasiamiehet voivat järjestää töitään. Perimisasiamiehet lisätään **Myyntireskontran parametrit** -sivulla valittuun ryhmään. Jos ryhmää ei ole valittu tällä sivulla, uusi **Perintä**-niminen ryhmä luodaan automaattisesti ja perimisasiamiehet lisätään kyseiseen ryhmään.

## <a name="set-up-a-writeoff-account"></a>Poistotilin määrittäminen
Määritä poistotili, jota käytetään kirjanpidon poistomerkinnässä, kun tapahtuma kirjataan pois. Tämä tili on tallennettu asiakkaan kirjausprofiiliin.

## <a name="set-up-nsf-information-for-bank-accounts"></a>NSF-tietojen määrittäminen pankkitilejä varten
Päivitä pankkitilit siten, että niillä on oikea kirjauskansion, kun NSF-maksuja havaitaan **Perintä**-sivulla. Valitse **Valuutan hallinta** -välilehden **NSF-maksukirjauskansio**-kentässä maksukirjauskansio.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Outlook-asetusten määrittäminen Perintä-sivun käyttäjille
Ennen kuin työntekijät voivat luoda tehtäviä tai lähettää sähköpostiviestejä **Perintä**-sivulla, sinun on varmistettava, että **Microsoft Outlook -synkronointi** -määritysavain on valittuna ja että Outlook-synkronointi on määritetty kyseisille työntekijöille.

## <a name="set-up-email-and-addresses"></a>Sähköpostin ja osoitteiden määrittäminen
Voit käyttää sähköpostia viestiessäsi sekä asiakkaiden että myyjien kanssa perintäongelmista sähköpostiviestien lähettämiseksi **Perintä**-sivulta. 

### <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Sähköposti- ja osoiteasetusten määrittäminen luotonvalvonnan yhteyshenkilöitä varten
Määritä asiakkaan yhteyshenkilöiden sähköpostiosoitteet, lähettääksesi sähköpostiviestejä kyseisille yhteyshenkilöille **Perintä**-sivulta. Perinnän yhteyshenkilöä käytetään oletusyhteyshenkilönä **Perintä**-sivulla. Voit määrittää tilioteosoitteen asiakkaalle, jos tiliotteissa on käytettävä ensisijaisesta osoitteesta poikkeavaa osoitetta. 

Valitse asiakkaan **Luotonvalvonta**-pikavälilehden **Korko ja maksukehotus -yhteyshenkilö** -välilehdessä perimiesasiamiehen kanssa työskentelevä asiakasorganisaation henkilö. Tätä henkilöä käytetään oletusyhteyshenkilönä **Perintä**-sivulla, ja sähköpostiviestit lähetetään hänelle. 

> [!NOTE] 
> Jos asiakkaalle ei ole määritetty perinnän yhteyshenkilöä, käytetään asiakkaan ensisijaista yhteyshenkilöä. Jos ensisijaista yhteyshenkilöä ei ole määritetty, sähköpostiviestit lähetetään **Yhteyshenkilöt**-sivulla ensimmäisenä olevaan sähköpostiosoitteeseen.

### <a name="set-up-email-settings-for-salespeople"></a>Sähköpostiasetusten määrittäminen myyjiä varten
Määritä myyjien sähköpostiosoitteet, lähettääksesi sähköpostiviestejä myyjille **Perintä**-sivulla. Määritä kunkin provisiomyyntiryhmän kunkin myyntiedustajan sähköpostiosoite. Myyntiedustaja, jolle on valittu **Perintä**-vaihtoehto, on oletusmyyjä, jolle sähköpostiviestit lähetetään. 

Jos myyntiedustajaa ei ole määritetty, käytetään asiakkaan organisaation ensisijaista myyjää. Jos ensisijaista myyjää ei ole määritetty, sähköpostiviestit lähetetään lomakkeessa ensimmäisenä olevalle myyjälle.


Lisätietoja on seuraavissa aiheissa:

 - [Maksukehotusjärjestyksen määrittäminen](tasks/create-collection-letter-sequence.md)

 - [Käsittele maksukehotuksia](tasks/process-collection-letters.md)

 - [Perimistietojen tarkistaminen](tasks/review-collections-information.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
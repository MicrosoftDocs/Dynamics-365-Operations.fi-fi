---
title: "Tuotannon suorittamisen rekisteröinti"
description: "Tässä aiheessa kuvataan tärkeitä käsitteitä ja termejä sinun on tiedettävä määrittäminen ja käyttäminen tuotannonohjausprosessi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: aee0a4eda2a2ac2f272f590781b9e751a8797095
ms.lasthandoff: 03/31/2017


---

# <a name="registration-for-manufacturing-execution"></a>Tuotannon suorittamisen rekisteröinti

Tässä aiheessa kuvataan tärkeitä käsitteitä ja termejä sinun on tiedettävä määrittäminen ja käyttäminen tuotannonohjausprosessi. 

Tuotannonohjaus on tarkoitettu ensisijaisesti tuotantoyritysten käytettäväksi. Työntekijät voivat rekisteröidä ajan ja nimikkeen kulutuksen tuotantotöissä **Työn rekisteröinti** -lomakkeella. Kaikki rekisteröinnit hyväksytään ja siirretään myöhemmin asianmukaisissa moduuleissa. Rekisteröintien jatkuva hyväksyntä ja siirto antavat esimiehille mahdollisuuden seurata helposti tuotantotilausten toteutuneita kustannuksia.

## <a name="manufacturing-execution-and-registration-terminology"></a>Tuotannonohjauksen ja rekisteröinnin käsitteistö
Seuraavassa taulukossa on tuotannonohjaukseen liittyviä termejä sekä liittyviä rekisteröintitehtäviä.

| Kausi                          | kuvaus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tuotannonohjaus       | Toiminto, jota käytetään rekisteröidä aika, materiaalin kulutuksen, tuotannon työt, projektit ja epäsuorat kustannukset. Rekisteröinti suoritetaan tuotannon suorittamisen rekisteröintiasiakasohjelmassa.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Työluettelo                      | **Työn rekisteröinti** -sivulla työntekijöille näytetään suoritettavien töiden luettelosta ne, jotka heidän on suoritettava tietyllä resurssilla, kuten laitteella. Työntekijä voi kirjata ajan ja nimikkeiden kulutuksen jokaiselle työlistassa olevalle työlle.                                                                                                                                                                                                                                                                                                                                                                           |
| Työn niputus                  | Jos työntekijä aloittaa useamman kuin yhden tehtävän samaan aikaan **Työn rekisteröinti** -sivulla, kutsutaan sitä niputustyöksi. Niputettuihin töihin käytettävä aika voidaan jakaa yksittäisille töille eri tavoin kohdistusavaimien avulla.                                                                                                                                                                                                                                                                                                                                                         |
| Vetäjän ja avustajan rekisteröinnit | Työntekijä voi rekisteröityä resurssin avustajaksi ja luoda pienen ryhmän, jossa useampi työntekijä työskentelee saman tuotannon työn parissa. Resursseja, joihin työntekijöitä liitetään, kutsutaan vetäjiksi. Ainoastaan vetäjäresurssin on tehtävä rekisteröinnit. Avustajat saavat samat rekisteröinnin automaattisesti. Jos esimerkiksi laite toimii vetäjänä, työntekijät, jotka on rekisteröity koneen avustajaksi voivat tehdä rekisteröinnit **Työn rekisteröinti** -sivulla, ja sekä kone että avustajiksi liitetyt työntekijät saavat samat rekisteröinnit. |
| Epäsuora tehtävä             | Tehtävä, joka ei liity suoraan tuotantotyöhön tai projektiin, kuten osastokokous, siivoustyö tai kunnossapitotyö. Työntekijöitä voi tehdä epäsuorien tehtävien rekisteröintejä samalla tavalla kuin he voivat rekisteröidä tuotannon töitä ja projekteja.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Rekisteröinnit valmistustoteutuksessa
Työntekijät voivat tehdä erityyppisiä rekisteröintejä tuotannonohjauksessa työlle, joka on suoritettu tuotantotöistä. Järjestelmän asetuksesta riippuen saattaa olla myös mahdollista, että työntekijät voivat suorittaa rekisteröintejä projektitehtäville ja tuottamattomille tehtäville, kuten tauoille, poissaololle ja epäsuorille tehtäville. Rekisteröintityypit ovat seuraavat:

-   **Saapuminen/poistuminen** (saatavilla työajan seurannassa) – Työntekijät tekevät saapumismerkinnän saapuessaan työhön ja poistumismerkinnän poistuessaan.
-   **Rekisteröi tuotantotöihin ** – Työntekijät voivat tehdä kirjauksia liittyen työlistassa oleviin tuotannon töihin, kuten aloittaa työn ja antaa palautetta työstä. Työntekijä voi aloittaa useita töitä samanaikaisesti. Tätä kutsutaan työn niputukseksi.
-   **Rekisteröi varastoon** – Työntekijät voivat tehdä rekisteröinnit työnohjauksessa käytetyistä materiaaleista, jotka eivät liity tuotantotöihin. Esimerkkejä ovat rasva, voiteluaineet tai muut materiaalit, joita käytetään koneiden käynnissä pitämiseen. Rekisteröinti tehdään varastokirjauskansiossa.
-   **Rekisteröityminen projekteihin** (saatavilla työajan seurannassa) – Työntekijät voivat tehdä rekisteröintejä liittyen työlistassa oleviin projekteihin tai projektin tehtäviin, kuten aloittaa ja lopettaa työn.
-   **Rekisteröidä projektimaksut ja projektinimikkeet** (käytettävissä, kello ja työajanseuranta) – työntekijät voivat rekisteröidä maksuja (kulut), jotka liittyvät projektin projektin maksukirjauskansio, kuten kilometrikorvaukset ja sillan maksullinen. Työntekijät voivat myös rekisteröidä nimikekulutuksen projektien Tämä suoritetaan projektinimikkeiden kirjauskansiossa.
-   **Rekisteröi toisen työntekijän avustajaksi** – Jos vähintään kaksi työntekijää toimii yhdessä tuotantotyössä tai projektissa, työntekijä voi rekisteröityä avustajana koneelle tai toiselle työntekijälle, joka toimii vetäjänä. Vetäjä voi tarvittaessa valita jonkin muun työntekijän vetäjäksi.
-   **Rekisteröi poissaolo** (saatavilla työajan seurannassa) – Työntekijät voivat rekisteröidä poissaoloajan määritetyillä poissaolokoodeilla. Poissaolon voi merkitä, kun työntekijä saapuu myöhässä, vaatii poissaolon työpäivän aikana tai lähtee normaalin työaikaprofiilikalenterin mukaan odotettua aiemmin.
-   **Rekisteröi tauot** (saatavilla työajan seurannassa) – Työntekijät voivat työaikana rekisteröidä lähtevänsä työpisteeltään tauolle. Useita vaihtotyyppejä voidaan määrittää. Kun työntekijä palaa ja kirjautuu sisään järjestelmään, järjestelmä rekisteröi työntekijän takaisin ja taukomerkinnän aika päättyy.
-   **Rekisteröi epäsuorat toiminnot** (saatavilla työajan seurannassa) – Epäsuorat toiminnot eivät liity suoraan tuotantoon, mutta joihin työntekijät voivat osallistua työpäivän aikana, kuten osaston tai tiimin kokous, tai työnohjauksessa suoritettava huoltotyö. Työntekijät voivat tehdä määritettyjen epäsuorien tehtävien rekisteröintejä.
-   **Rekisteröi ylityö** (saatavilla työajan seurannassa) – Ylitöihin pyydetyt työntekijät voivat merkitä ylityötuntinsa joustavaksi työajaksi tai ylitöiksi.




---
title: Warehouse Management -mobiilisovelluksen uudet ja muuttuneet ominaisuudet
description: Tässä aiheessa luetellaan jokaisen Microsoft Dynamics 365 Supply Chain Managementin Warehouse Management -mobiilisovelluksen vapautetun version uudet ja muuttuneet ominaisuudet.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261774"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Warehouse Management -mobiilisovelluksen uudet ja muuttuneet ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä aiheessa luetellaan ominaisuudet, korjaukset, parannukset ja tunnetut ongelmat jokaisen Microsoft Dynamics 365 Supply Chain Managementin Warehouse Management -mobiilisovelluksen vapautetun version osalta.

## <a name="version-2060"></a>Versio 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Uudet ominaisuudet, korjaukset ja parannukset versiossa 2.0.6.0

Tämä versio sisältää seuraavat uudet ominaisuudet, korjaukset ja parannukset:

- Demotila näyttää nyt kaikki etiketit laitteen kielellä.
- Näyttöön tulee vähemmän todennäköisesti seuraava virhesanoma: "Sopivaa näkymää ei pystytä näyttämään määritetyssä koossa".
- Työkorttien vähimmäiskorkeus on kasvanut (jos työluettelossa on määritetty näkymään vähintään kolme kenttää).
- Tietokorttien alaosassa olevia marginaaleja (häivytetään) on parannettu.
- Palvelimessa vaihdeltavat XML-tiedostojen virheelliset symbolit käsitellään nyt onnistuneesti. (Esimerkiksi tulostettavat merkit käsitellään nyt onnistuneesti, eikä sovelluksen enää tarvitse lopettaa vastaamista.)
- HTTP-virheet (kuten virhe 503), kun palvelinpyyntö lähetetään, käsitellään nyt onnistuneesti.
- Kun näyttöön tulee virhe, vaihtoehtoluetteloa ei enää näytetä automaattisesti yhdistelmäruudun ohjausobjekteille.
- Sovellus ei enää lakkaa vastaamasta käyttäjäasetuksissa on valittu näytön suunnan vuoksi.
- Tuotekuvat näkyvät nyt itsepalveluympäristöissä. (Tämä muutos koskee vain matalan resoluution versioita. Tiedostonhallintapalvelu ei tue täysikokoisia kuvia itsepalveluympäristöissä.)
- Ongelma, johon liittyi nollamäärän lyhyitä poimintoja, on korjattu.
- Sovellus ei enää lakkaa vastaamasta, kun tietokortissa näkyy useita samanlaisia kenttiä.

### <a name="known-issues-in-version-2060"></a>Tiedossa olevat virheet versiossa 2.0.6.0

Tässä versiossa on seuraavia tiedossa olevia virheitä:

- Sovellus (erityisesti työluettelo) hidastuu ajan mittaan.
- **Windows-versio:** Kun skannaukseen käytetään USB-asetta Windowsissa, epäjohdonmukaiset tulokset aiheuttavat skannattujen symbolien sekoittumisen.

## <a name="version-2050"></a>Versio 2.0.5.0

Tämä versio sisältää seuraavat uudet ominaisuudet, korjaukset ja parannukset:

- Asiakasohjelma ei ole enää piilotettu yhteysasetusten määritysten avulla.
- Voit nyt painaa pitkään mitä tahansa tekstiä, jos haluat nähdä sen kokonaan.
- Virheilmoitusta on parannettu, kun tallennuskäyttöoikeudet puuttuvat.
- Joihinkin työnkulkuihin on lisätty uusia ohjaussarjoja.
- Lähetyspainiketta ei enää voi käyttää virheellisesti ikkunan koon vuoksi.
- Liukusäätimien käyttöä voi nyt jatkaa pienemmillä näytöillä, kun käytössä on suurempia painikekokoja.
- Nelipainikkeen peittoa ei enää ole katkaistu.
- Näppäimistö tukee nyt Poista-painiketta.
- Kirkkausongelma, joka voi ilmetä näppäimistöä painettaessa, on korjattu.
- Erilaisia demotietojen ongelmia on korjattu.
- Ongelma, johon tietosivun numeeriset kentät vaikuttavat, on korjattu.
- Näyttönäppäimistön käyttö ei enää ajoittain poistu näkyvistä joillakin laitteilla.
- Erilaisia käyttöliittymävikoja (UI) on korjattu, kuten virheitä, jotka vaikuttivat taustaväriin ja asemointiin.
- Venäjänkielistä käyttöliittymää on parannettu.
- Useita ongelmia, jotka saivat järjestelmän lopettamaan vastaamisen, on korjattu.
- Laskimen avaamiseen uudelleen liittyvä ongelma on korjattu.
- **Android-versio:** Virhe, joka aiheutti sen, että Android 4.4-versio lopetti vastaamisen käynnistyksen yhteydessä, on korjattu.
- **Android-versio:** Vähimmäisskaalaus on vähennetty 50 prosentiksi.

## <a name="version-2040"></a>Versio 2.0.4.0

Versio 2.0.4.0 on Warehouse Management -mobiilisovelluksen ensimmäinen yleisesti saatavilla oleva versio.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Uudet ominaisuudet, korjaukset ja parannukset versiossa 2.0.4.0

Tässä versiossa esitellään seuraavat uudet ominaisuudet, korjaustiedostot ja parannukset, jotka eivät ole käytettävissä esiversiossa:

- Jos tietokortissa on kaksi etikettiä, joissa on samanlaiset tiedot, toinen etiketistä piilotetaan.
- Oletusarvon mukaan näytetään erikoismerkit, ja niiden piilovaihtoehto on poistettu käyttäjän asetuksista.
- Käytöstä poistetut lähetyspainikkeet näytetään nyt niin, että ne eivät ole käytettävissä tässä näkymässä.
- Muutokset ohjausobjektien järjestyksen logiikkaan varmistavat, että laitteiden skaalaukset ovat joustavampia. Fonttien tai painikkeiden skaalaamista ei tarvitse enää muuttaa.
- Oletusväriteema on muutettu *tummaksi*.
- Käytöstä poistettujen lähetyspainikkeiden puuttuva kuvake on lisätty nauhanäkymään.
- Aikakatkaisupoikkeukset vievät nyt yhteyssivulle linjavirheen näyttämisen sijaan.
- Jos lähetystoimintoa ei ole käytettävissä (esimerkiksi **OK**, **Kyllä**, **Hyväksy**, **Valmis** tai **Valmis**), lähetyspainike poistetaan käytöstä.
- Sovelluksen vakautta on parannettu.
- [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701) -suojausongelmat voidaan korjata.
- **Windows-versio:** Windows-ongelma, jonka valikot eivät olleet responsiivisia ikkunan muuttamisen jälkeen, on korjattu.

### <a name="known-issue-in-version-2040"></a>Tiedossa oleva virhe versiossa 2.0.4.0

Tässä versiossa on seuraava tiedossa oleva virhe:

- Tässä versiossa on ongelma, joka koskee laitteita, jotka käyttävät Android 4.4 -versiota. Saatat kohdata ongelmia, kun käytät sovellusta tässä Android-versiossa.

---
title: Virhe todennuspolussa määritettäessä sovellusyhteyttä
description: Jos Warehouse Management -sovelluksessa näkyy virhe "Todennuspolun luottamusankkuria ei löydy", voit ratkaista tai korjata ongelman tämän sivun avulla.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476231"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Todennuspolun luottamusankkuria ei löydy määritettäessä sovellusyhteyttä

## <a name="symptoms"></a>Oireet

Kun yrität muodostaa yhteyttä Supply Chain Managementiin, Warehouse Management -sovellus saattaa antaa seuraavan virhesanoman:

> java.security.cert.certPathValidatorException: Varmennepolun luottamusankkuria ei löydy.

Tämä ongelma voi vaikuttaa laitteisiin, joilla on seuraavat ominaisuudet:

- **Käyttöjärjestelmän versio**: Android 4.4.x (kuten Zebra TC55). Tämä ei ole ongelma viimeaikaisissa Android-versioissa.
- **Supply Chain Managementin sijainti**: Pilvi
- **Yhteystila**: Asiakasohjelman salasana tai varmenne

## <a name="possible-cause"></a>Mahdollinen syy

Microsoft on saattanut päivittää Supply Chain Managementin käyttämiä palvelimen SSL-varmenteita. Tästä syystä päävarmenne ja/tai jokin väliaikaisista varmenteista on ehkä muuttunut, joten uusi varmenne ei ole matkapuhelimen luotettujen järjestelmävarmenteiden luettelossa. Uudemmat Android-versiot päivittävät luotettujen varmenteiden luettelon automaattisesti, mutta Android4.4.x ei.

## <a name="resolution"></a>Ratkaisu

Ratkaise ongelma seuraavalla tavalla:

- Päivitä kukin laite käyttämällä seuraavassa osassa kuvattua kiertotapaa.
- Zebralta tai Googlelta *voi* olla mahdollista saada päivitys järjestelmän luotettujen varmenteiden myöntäjien varmenteisiin. Tätä ei kuitenkaan ole vahvistettu.
- Harkitse mahdollisuuksien mukaan vanhojen laitteiden korvaamista uudempaa Android-versiota käyttävillä laitteilla (jossa luettujen varmenteiden myöntäjien varmenteiden luetteloa päivitetään automaattisesti).

### <a name="workaround"></a>Ongelman kiertäminen

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>Vaihe 1: Uuden päävarmenteen vieminen Supply Chain Managementista

Lataa uusi päävarmenne manuaalisesti internetselaimesi avulla seuraavasti:

1. Kirjaudu Dynamics Supply Chain Managementiin ja avaa etusivu.

1. Valitse selaimen osoitepalkissa kuvake, jolla avataan **Sijainti on turvallinen** -valintaruutu.
1. Valitse valintaruudussa **Varmenne (kelvollinen)** avataksesi kulloisenkin varmenteen **Varmenne**-ikkunan.
1. Avaa **Varmenne**-ikkunan **Varmennepolku**-välilehti.
1. Valitse hierarkian ylin varmenne. (se on päävarmenne).
1. Avaa **Varmenne**-ikkunan **Tiedot**-välilehti.
1. Valitse **Kopioi tiedostoon** -painike **Tiedot**-välilehden alareunasta.
1. **Ohjattu varmenteen vientitoiminto** avautuu. Jatka valitsemalla **Seuraava**.
1. **Vie tiedostomuoto** -sivu aukeaa. Valitse **DER-koodattu binaari X.509 (.CER)**. Jatka sitten valitsemalla **Seuraava**.
1. **Vietävät tiedostot** -sivu avautuu, määritä tiedostonimi ja -sijainti. Jatka sitten valitsemalla **Seuraava**.
1. **Valmistellaan varmenteen viennin ohjattu toiminto** -sivu avautuu ja näkyvissä on viennin tulos. Valitse **Valmis**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>Vaihe 2: Ladatun varmenteen asennus asianomaisille laitteille

Asenna ladattu varmenne seuraavasti:

1. Siirrä edellisessä vaiheessa lataamasi varmenne päivitettävään laitteeseen. Voit käyttää esimerkiksi SD-korttia tai verkkoyhteyttä asettaaksesi tiedoston laitteesi käytettäväksi.
1. Avaa laitteen suojausasetukset ja valitse valikosta vaihtoehto asentaa varmenne tiedostosta. (Tämän tarkat vaiheet vaihtelevat laitteen ja käyttöjärjestelmän version mukaan.)
1. Uuden varmenteen pitäisi nyt näkyä luotettujen varmenteiden **Käyttäjä**-välilehdessä.
1. Toista tämä toimenpide jokaisen asianosaisen laitteen osalta.

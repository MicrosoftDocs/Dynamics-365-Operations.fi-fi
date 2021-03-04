---
title: Päivitä ylläpitobudjetit
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitobudjetti päivitetään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e43abd4644eec8c91606ec48bbecf30f12600856
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427136"
---
# <a name="update-maintenance-budgets"></a>Päivitä ylläpitobudjetit

[!include [banner](../../includes/banner.md)]

 

**Ylläpitobudjetin rivit** -sivulla näkyvät kaikki budjettirivit, jotka on luotu **Ylläpitobudjetit**-sivulla valitulle budjetille. (Lisätietoja on kohdassa [Luo ylläpitobudjetit](create-maintenance-budget.md)luominen.) Voit laskea uudelleen ja oikaista kunnossapitobudjetin rivejä, kunnes ylläpitobudjetti on hyväksytty. Kun budjettikausi on kulunut ja kustannukset on kirjattu käyttöomaisuuden hallinnassa, voit myös päivittää todelliset kustannukset budjettiriveille.

## <a name="recalculate-a-maintenance-budget"></a>Laske ylläpitobudjetti uudelleen

Kunnossapitobudjetin voi laskea uudelleen **Ylläpitobudjetin rivit** -sivulla. Kun huoltobudjetti lasketaan uudelleen, olemassa olevat budjettirivit poistetaan ja uusi laskenta tehdään.

1. Valitse **Ylläpitobudjetin rivit** -sivulla **Laske uudelleen**.
2. Tee uuden laskennan edellyttämät muutokset **Laske budjetti uudelleen** -valintaikkunassa ja valitse sitten **OK**.

Uudet budjettirivit luodaan määrittämiesi arvojen mukaan.

## <a name="adjust-budget-lines"></a>Budjettirivien oikaisu

Koko kunnossapitobudjetin uudelleenlaskemisen asemesta voit oikaista valittuja budjettikustannuksiin liittyviä rivejä.

1. Valitse **Ylläpitobudjetin rivit** -sivulla rivit, joille haluat päivittää budjetin kustannukset.
2. Valitse **Oikaise**.
3. Jos haluat lisätä summan valittuihin riveihin, valitse **Lisää kustannus** -valintaruutu ja kirjoita sitten arvo **Lisää arvo** -kenttään.
4. Jos haluat kertoa valittujen budjettirivien budjetoidut kustannukset kertoimella, valitse **Kerro kustannukset** -valintaruutu ja kirjoita kerroin **Kertoimen arvo** -kenttään.

    Jos esimerkiksi kirjoitat **1,2**-arvon **Kertoimen arvo** -kenttään, korotat valittujen rivien budjetin kustannuksia 20 prosentilla. Jos syötät **0,7**, vähennät valittujen rivien budjetin kustannuksia 30 prosentilla.

5. Valitse **OK**.

Valitut budjettirivit päivitetään vaiheessa 3 tai 4 määritettyjen arvojen mukaisesti.

## <a name="update-actual-costs"></a>Päivitä toteutuneet kustannukset

Kun budjettirivien päivämäärät ovat ohi ja toteutuneet kustannukset on kirjattu käyttöomaisuuden hallinnassa, voit myös päivittää todelliset kustannukset ylläpitobudjettiin.

1. Valitse **Ylläpitobudjetin rivit** -sivulla **Päivitä kustannukset**.
2. Valitse **Laske toteutunut kustannus** -valintaikkunassa **OK**.

Budjettirivien **Toteutunut kustannus** -kentät päivitetään, jos todelliset kustannukset on kirjattu. Uusia budjetti rivejä voidaan luoda, jos uusia käyttöomaisuustyyppejä on luotu sen jälkeen, kun olet luonut budjetin, ja jos näitä käyttöomaisuuslajeja on käytetty sellaisten omaisuuserien osalta, joille on luotu työtilauksia ja joihin liittyvät kustannukset on kirjattu. Uusilla budjettiriveillä näkyvät vain todelliset kustannukset, koska niille ei laskettu budjettikustannuksia.

> [!NOTE]
> Jos haluat nähdä yhteenvedon todellisista kustannuksista, jotka on jaettu ennaltaehkäiseviin, korjaaviin ja investointikustannuksiin, voit tehdä saman kauden laskun **Resurssien kustannusten hallinta** -sivulla. 

## <a name="manually-add-budget-lines"></a>Budjettirivien lisääminen manuaalisesti

**Ylläpitobudjetin rivit** -sivulla voit lisätä uuden budjettirivin manuaalisesti valitsemalla **Uusi** ja tekemällä sitten valintoja rivillä. Seuraavassa on esimerkkejä tilanteista, joissa tästä lähestymistavasta voi olla hyötyä:

- Tiedät, että joidenkin käyttöomaisuuserien kunnostus on parhaillaan suunnitteluvaiheessa, mutta siihen liittyviä töitä ei ole vielä luotu omaisuuden hallinnassa. Haluat kuitenkin, että näiden töiden budjettikustannukset sisällytetään ylläpitobudjettiin.
- Uusia resursseja tai resurssityyppejä on luotu ylläpitobudjetin luomisen jälkeen, mutta ylläpitosuunnitelmia ei ole vielä määritetty näille käyttöomaisuuserille tai -tyypeille. Haluat kuitenkin, että näiden resurssityyppien budjettikustannukset sisällytetään ylläpitobudjettiin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
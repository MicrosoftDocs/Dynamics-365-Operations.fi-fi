---
title: Toimintojen tuominen yleisestä tietovarastosta
description: Tässä artikkelissa kerrotaan, miten globalisointitoiminnot tuodaan yleistietovarastosta.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: bc8f346cdef4aa0b909d75b016b37cbbe3248ebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865552"
---
# <a name="import-features-from-the-global-repository"></a>Toimintojen tuominen yleisestä tietovarastosta

[!include [banner](../includes/banner.md)]

Yleinen tietovarasto sisältää konfiguroinnin palveluntarjoajalle jaettuja sähköisen laskutuksen toimintoja. Kaikki Microsoftin tarjoamat sähköiset laskutustoiminnot jaetaan kaikkien yritysten kanssa. Saat automaattisesti käyttöoikeudet kaikkiin sähköisiin laskutusominaisuuksiin, jotka Microsoft julkaisee ja julkaisee yleisessä tietovarastossa.

Voit aloittaa työskentelyn konfiguroinnin palveluntarjoajalle jaetuilla sähköisillä laskutusominaisuuksilla tuomalla ne Regulatory Configuration Service (RCS) -esiintymään yleisestä tietovarastoista. Tarkista sitten toiminnon tiedot, kuten sähköisen raportoinnin (ER) konfiguraatiot ja käsittelyputket.

## <a name="import-a-feature-from-the-global-repository"></a>Toiminnon tuominen yleisestä tietovarastosta

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatio-ominaisuus** -työtilan **Toiminnot**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Tuo** avataksesi **Tuo toiminto yleisestä tietovarastosta**-haun.
4. Synkronoi organisaation RCS-esiintymä valitsemalla **Synkronoi**, kun haluat selata tietyn konfiguraation tarjoajan yleisessä tietovarastossa käytettävissä olevia sähköisiä laskutustoimintoja. Kun synkronointi on valmis, käytettävissä olevien sähköisten laskutusominaisuuksien luettelo päivitetään yleisestä tietovarastosta. Tämä päivitys voi kestää muutamia minuutteja.
5. Valitse tuotava ominaisuus ja valitse sitten **Tuo**.

Voit tarkastella tuotua sähköisen laskutuksen ominaisuutta varmistamalla, että oikea konfiguraatiopalvelu on valittu. Oletusarvon mukaan aktiivisen konfiguraation tarjoajan luomat ominaisuudet suodatetaan automaattisesti. Voit muokata suodatinta ja tarkastella muiden palveluntarjoajien, kuten Microsoft-konfiguraationtarjoajan, luomia ominaisuuksia.

Voit nyt käyttää tuotua toimintoa. Voit tarkistaa sen tiedot ja luoda uuden ominaisuuden käyttämällä tuotua ominaisuutta mallina.

> [!NOTE]
> Voit muokata toimintoa vain, jos sen on luonut konfiguraatiopalvelu, joka on aktiivinen. Voit luoda uuden ominaisuuden käyttämällä alkuperäistä ominaisuutta perustana. Tämän jälkeen voit tehdä tarvittavat muutokset tai määrittää parametrit.

Kun Microsoft tai muu yritys, joka jakaa globalisointiominaisuuksia yrityksellesi, päivittää tuodut toiminnot, voit tarkistaa päivitetyt versiot valitsemalla **Tarkista toimintopäivitykset** **Globalisointiominaisuudet**-työtilan **Aiheeseen liittyviä asetuksia** -osasta.

Jos näet, että mallina käytettävää toimintoa varten on päivityksiä, voit tuoda uuden version sen jälkeen, kun olet synkronoinut yleisen tietovaraston julkaistujen ominaisuuksien luettelon.

---
title: Rekisteröi nimikkeet perusvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota
description: Tässä menettelyssä kerrotaan, miten nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallintamoduulin perusvarastointi.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c36513587754939da4e1791b687871f71e7e8fa3d3e9990609cb7ede1c32cc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760223"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Rekisteröi nimikkeet perusvarastointikäyttöön tarkoitetuksi nimikkeiksi käyttäen nimikkeen saapumisen kirjauskansiota

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten nimikkeet rekisteröidään käyttämällä nimikkeen saapumisen kirjauskansiota, kun käytössä on varastonhallintamoduulin perusvarastointi. Vastaanottoassistentti tekee yleensä tämän tehtävän. Voit suorittaa tämän menettelyn esittelytietojen USMF-yrityksen avulla näkyvillä olevilla esimerkkiarvoilla.  Jos et käytä USMF-yritystä, sinun on vahvistettava ostotilaus ja avoimen ostotilauksen rivi, ennen kuin aloitat tämän ohjauksen suorittamisen. Rivin nimike on varastoitava. Nimike on myös liitettävä varastodimensioryhmään, jonka toimipaikka ja varasto ovat aktiivisia.


## <a name="create-item-arrival-journal-header"></a>Nimikkeen saapumisen kirjauskansion otsikon luominen
1. Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Nimikkeen saapuminen > Nimikkeen saapuminen.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
    * Jos käytössä on USMF, voit syöttää arvoksi WHS. Jos käytät muita tietoja, kirjauskansiolla, jonka nimen valitsit, on oltava seuraavat ominaisuudet: Tarkista keräilysijainti -asetukseksi on määritettävä Ei ja Karanteeninhallinta-asetukseksi Ei.  
4. Kirjoita arvo Pakkausluettelo-kenttään.
    * Tämä on toimittajan luoman pakkausluettelon tunnus. Lisää yksilöivä numero.  
5. Valitse Numero-kenttään ostotilaus.
6. Valitse OK.

## <a name="add-lines-to-item-arrival-journal"></a>Rivien lisääminen nimikkeen saapumisen kirjauskansioon
1. Valitse Toiminnot.
2. Valitse Luo rivit.
    * Tämän kirjauskansion rivit voidaan syöttää manuaalisesti tai luoda automaattisesti. Tässä osassa kerrotaan, miten rivit luodaan automaattisesti.  
3. Valitse Alusta määrä -valintaruutu tai poista sen valinta.
    * Tämä alustaa niiden kirjauskansiorivien määrän, joiden määrää ei ole rekisteröity ostotilausriviltä.  
4. Valitse OK.

## <a name="post-the-journal"></a>Kirjaa kirjauskansio
1. Valitse Kirjaa.
2. Valitse OK.

## <a name="generate-the-product-receipt"></a>Tuotteen vastaanoton luominen
1. Valitse Toiminnot.
2. Valitse Tuotteen vastaanotto.
3. Valitse OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
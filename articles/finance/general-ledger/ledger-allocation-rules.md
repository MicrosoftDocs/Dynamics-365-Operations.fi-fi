---
title: Kirjanpidon kohdistussäännöt
description: Tässä artikkelissa on tietoja kirjanpidon kohdistussäännöistä. Artikkelissa kuvataan kohdistussääntöjen eri osia sekä käytettävissä olevia kohdistussääntöjä.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: kfend
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0691c65e6a499f713952070811cefaa7a213af7b
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787550"
---
# <a name="ledger-allocation-rules"></a>Kirjanpidon kohdistussäännöt

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja kirjanpidon kohdistussäännöistä. Artikkelissa kuvataan kohdistussääntöjen eri osia sekä käytettävissä olevia kohdistussääntöjä.

Kirjanpidon kohdistussääntöjen avulla voidaan automaattisesti laskea ja luoda kohdistuskirjauskansioita ja kirjanpitomerkintöjä kirjanpitosaldojen tai kiinteiden summien kohdistusta varten. Kohdistusmenetelmät voivat olla muuttuvia tai kiinteitä. Kohdistus perustuu tapahtuman valuutta-arvoon. Esimerkiksi ulkomaan valuutan voiton/tappion kirjaukset merkitään kirjanpidon ja raportointivaluuttamäärien oikaisemiseksi. Näitä merkintöjä ei sovelleta kohdistussääntöihin, koska niiden tapahtumavaluutta-arvo on 0,00. Kirjanpidon kohdistussäännöissä voidaan käyttää seuraavia kohdistusmenetelmiä:

-   **Peruste** – Tätä muuttuvaa menetelmää käytetään, kun kohdistus riippuu todellisesta kirjanpitosaldosta suodatusehtojen perusteella. Esimerkiksi mainoskulut voidaan kohdistaa sen mukaan, mikä on kunkin osaston myynti suhteessa osastojen kokonaismyyntiin.
-   **Kiinteä prosentti** ja **kiinteä paino** – Näissä menetelmissä kohdistusprosentti tai paino on määritetty suoraan säännölle. Esimerkiksi mainontakulut voidaan kohdistaa siten, että osasto A saa 70 prosenttia mainoskuluista ja osasto B 30 prosenttia.
-   **Tasaisesti** – Tämä menetelmä jakaa summan tasan kunkin määritetyn kohteen kesken. Jos esimerkiksi kohteita määritetään osastolle A ja B, mainoskulut voidaan jakaa siten, että osastot A ja B saavat kumpikin 50 prosenttia mainoskuluista.

Jos kohdistussäännön kohdistusmenetelmä on Peruste, myös erilliset kirjanpidon kohdistusperustesäännöt täytyy määrittää. Käsittele kohdistuspyyntö -prosessin avulla käyttäjät voivat käsitellä kirjanpidon kohdistussäännön ja esikatsella tuloksena muodostuvia kohdistuksen kirjauskansiovientejä, ennen kuin he joko kirjaavat tai poistavat lasketut kohdistukset.

## <a name="components-of-ledger-allocation-rules"></a>Kirjanpidon kohdistussääntöjen osat
Jokaisella kohdistussäännöllä on neljä komponenttia: yleinen, lähde, kohde ja vastakirjaus. Lisäkomponenttina tarvitaan kirjanpidon kohdistusperustesäännöt, jos kohdistusmenetelmänä on Peruste. Jokainen komponentti tarjoaa tärkeitä tietoja, jotka tarvitaan kohdistusten käsittelemiseen.

-   **Yleinen** – Tässä komponentissa käyttäjä määrittää vaihtoehdot, kuten kohdistusmenetelmän, konsernin sisäisten sääntöjen asetukset ja sen, onko sääntö aktiivinen.
-   **Lähde** – Tässä komponentissa käyttäjä määrittää kohdistuksen lähdetiedot. Varaus voi perustua kirjanpitosaldoihin (**Tietolähde**  =  **Kirjanpito**) tai kiinteisiin summiin (**Tietolähde**  =  **Kiinteä arvo**). Kun **Tietolähde** -asetukseksi valitaan **Kirjanpito**, kirjanpidon kohdistussäännölle (esimerkiksi mainoskuluille) on määritettävä lähteen suodatusehdot.
-   **Kohde** – Tämä komponentti määrittää, miten kohdistuksen laskennan tulos jaetaan ja kirjataan. Kullekin osastolle voi esimerkiksi olla yksi kohderivi.
-   **Vastakirjaus** – Tämä komponentti määrittää, miten päätilit ja dimensiot pitää määritellä vastakirjauksille, joilla kohdekirjaukset täsmätään. Käyttäjän määrittämiä vaihtoehtoja käytetään tavallisesti lähteeseen perustuvien tilien ja dimensioiden sijasta. Kun **Tietolähde**-asetuksena on **Kiinteä arvo**, **Lähde**-vaihtoehtoa ei voi käyttää.
-   **Kirjanpidon kohdistusperustesäännöt** – Näillä säännöillä on omat lähteen suodatusehdot, jotka määrittävät, mitä kirjanpitosaldoja käytetään kohdistuksessa (esimerkiksi tuotto osastoittain). Kutakin kohdistusperusteen sääntöä voi käyttää useiden kohdistussääntöjen kanssa.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]

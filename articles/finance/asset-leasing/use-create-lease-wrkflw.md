---
title: Vuokrauksen hyväksyntätyönkulkujen käyttäminen
description: Tässä ohjeaiheessa kerrotaan, miten työnkulkuja käytetään resurssin vuokrausten hyväksymisessä ja miten työnkulkujen tilaa ja historiaa seurataan.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1086231c65a726df5162d3593419a129d6ae5655
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992755"
---
# <a name="use-lease-approval-workflows"></a>Vuokrauksen hyväksyntätyönkulkujen käyttäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten työnkulkuja käytetään resurssin vuokrausten hyväksymisessä ja miten työnkulkujen tilaa ja historiaa seurataan. Työnkulkujen avulla vuokrasopimusten hyväksyntöjen hallinta on yhdenmukaista, koska käytössä on vakiohyväksyntävaiheet ja tietty käyttäjä, joka hyväksyy prosessin jokaisen vaiheen. Hyväksyjä voi hyväksyä vuokrasopimuksen, hylätä sen, pyytää siihen muutosta tai määrittää sen toiselle käyttäjälle hyväksyttäväksi. Työnkulut voivat myös tuoda hyväksyntäprosessiin lisää näkyvyyttä, kun niiden tilaa ja historiaa seurataan. Lisäksi voit tarkastella keskitettyä työluetteloa, jossa ovat tietyille hyväksyjille määritetyt tehtävät ja hyväksynnät.

Ennen kuin käytät tätä menetelmää, varmista, että ainakin vuokrasopimuksen hyväksyntätyönkulku on luotu. Jos työnkulkua ei ole, luo se. Lisätietoja työnkulun määrittämisestä on kohdassa [Vuokrasopimuksen hyväksyntätyönkulkujen määrittäminen](set-up-lease-wrkflw.md).

1. Lähetä vuokrasopimus hyväksyttäväksi. Valitse vuokrasopimuksen **Kirjan tiedot** -sivulla **Työnkulku** ja valitse sitten **Lähetä**.
2. Näyttöön tulevaan valintaikkunaan voit lisätä kommentin. Määritetty hyväksyjä näkee tämän kommentin yhdessä vuokrasopimuksen kanssa. Kun olet kirjoittanut kommentin, valitse **Lähetä**. Vuokrasopimus lähetetään työnkulkujärjestelmään, ja hyväksyjä saa sen hyväksyttäväksi.
3. Jos haluat nähdä ne vuokrasopimukset, jotka ne on määritetty hyväksyttäväksi, siirry kohtaan **Moduulit \> Yleiset \> Työnimikkeet \> Minulle määritetyt työnimikkeet**.
4. Valitse **Minulle määritetyt työnimikkeet** -sivulla sen vuokrasopimuksen **Vuokrasopimuksen tunnus** -linkki, jota haluat tarkastella. Näkyviin tuleva sivu määräytyy niiden vuokrauskirjojen ja -tietojen perusteella, joiden käyttöoikeus käyttäjällä on.
5. Kun olet lopettanut vuokrasopimuksen tarkastelun, valitse **Työnkulku** ja päätä, mihin toimiin on ryhdyttävä. Vaihtoehtoja ovat **Hyväksy**, **Hylkää**, **Pyydä muutosta**, **Delegoi** ja **Peruuta**. Voit myös valita **Tarkastele historiaa**, jos haluat tarkastella valitun vuokrasopimuksen historiaa.
6. Kun olet valinnut toiminnon, anna sitä kuvaava kommentti. Kun olet antanut kommentin, valitse **Hyväksytty**-toiminto luettelosta.
7. Voit tarkastella hyväksymistoimintoja siirtymällä takaisin **Vuokrasopimuksen tiedot** -sivulle **Vuokrasopimusyhteenveto**-sivulta ja valita sitten **Työnkulku \> Tarkastele historiaa**.

    Voit tarkastella työnkulun aktiviteetteja **Työnkulkuhistoria**-sivulla. Tällä sivulla näkyvät tiettyyn vuokrasopimukseen tehdyt työnkulun vaiheet. Voit tarkastella määritettyjen työnimikkeiden tilaa myös **Työnimikkeet**-kentän avulla.

8. Jos haluat pysäyttää työnkulun, valitse **Työnkulun historia** -sivulla **Saanti**. Syötä näkyviin tulevassa valintaikkunassa kommentti ja valitse sitten **OK**.
9. Jos haluat poistaa työnkulun aktivoinnin tai aktivoida aiemmin luodun työnkulun, siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokrauksen työnkulku**. Valitse sitten **Vuokrauksen työnkulku** -sivulla **Työnkulku \> Versiot**. Jos haluat poistaa nykyisen työnkulun aktivoinnin, valitse aktiivinen vuokrasopimus vuokrasopimusversion valintaikkunassa ja valitse sitten **Poista aktivointi**. Jos haluat määrittää aiemmin luodun työnkulun aktiiviseksi, valitse työnkulku ja valitse sitten **Määritä aktiiviseksi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
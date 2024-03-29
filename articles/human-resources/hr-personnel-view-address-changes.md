---
title: Osoitemuutosten tarkasteleminen ja hallinta
description: Tässä artikkelissa kerrotaan, kuinka voit tarkastella ja hallita Dynamics 365 Human Resources -järjestelmän osoitemuutoksia.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 744ab532fcc663f25ce376817779924bbef15432
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899582"
---
# <a name="view-and-manage-address-changes"></a>Osoitemuutosten tarkasteleminen ja hallinta


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kerrotaan, kuinka voit tarkastella ja hallita osoitemuutoksia **Muokkaa henkilökohtaisia tietoja** -sivulla (joka avataan **Työntekijän itsepalvelu** -työtilassa) tai **Työntekijän tiedot** -sivulla Dynamics 365 Human Resourcesissa.

Monet organisaatiot haluavat, että työntekijät voivat hallita omia henkilötietojaan itsepalvelukokemuksen kautta. Voit sallia käyttäjien päivittää osoitteensa **työntekijän itsepalvelu** -työtilassa. Tämän jälkeen voit seurata muutoksia **henkilöstöhallinnan** työtilassa. Jotta voisit käyttää tätä toimintoa, sinun on määritettävä, kuinka monta päivää haluat tarkastella muutoksia **henkilöstöhallinnon parametrit** -sivulla.

## <a name="configure-address-change-parameters"></a>Osoitteenmuutosparametrien määrittäminen

Voit määrittää, montako päivää haluat osoitteiden muutosten näkyvän **henkilöstöhallinnan** työtilassa, toimimalla seuraavasti:

1. Valitse siirtymisruudussa **henkilöstöhallinto**.
2. Valitse **Linkit**.
3. Määritä **henkilöstöhallinnon parametrit**.
4. Kirjoita osoitteenmuutoskohdan **päivien määrä** -kenttään päivien määrä, jonka haluat **osoitteen muutosten** näkyvän **henkilöstöhallinnon** työtilassa.
5. Sulje sivu.

## <a name="create-or-change-an-employee-address"></a>Työntekijän osoitteen luominen tai muuttaminen

Työntekijät voivat päivittää osoitteensa **työntekijän itsepalvelu** -työtilassa. Noudata seuraavia ohjeita luodaksesi tai muuttaaksesi osoitetta:

1. Valitse **Työntekijän itsepalvelu** -ruutu **aloitussivulla**.
2. Valitse **Muokkaa henkilökohtaisia tietoja**.
3. Valitse **Lisää** lisätäksesi osoitteen. Jos haluat päivittää aiemmin luotua osoitetta, valitse osoite listasta ja valitse sitten **Muokkaa**.
4. Kirjoita **Nimi tai kuvaus**.
5. Valitse **Tarkoitus** avattavasta luetteloruudusta ja valitse sitten osoitetyyppi.
6. Syötä **Maa/alue**.
7. Kirjoita **postinumero**.
8. Kirjoita **katuosoite**.
9. Kirjoita **paikkakunta**, **osavaltio** ja **alue**. Yleensä nämä kentät määritetään automaattisesti **Postinumero**-kentän perusteella.
10. Vaihtoehtoisesti voit valita ensisijaisen osoitteen **ensisijaiselle** kentälle. Vain yksi osoite voidaan merkitä ensisijaiseksi. Jos toinen osoite on jo merkitty ensisijaiseksi osoitteeksi, sinun on vahvistettava, että haluat käyttää tätä osoitetta ensisijaisena.
11. Vaihtoehtoisesti voit valita yksityisen osoitteen **yksityiselle** kentälle. Vain käyttäjät, joilla on nimenomainen oikeus tarkastella yksityisiä osoitetietoja, voivat tarkastella tätä osoitetta.
12. Valitse **OK**.

## <a name="create-or-change-a-worker-address"></a>Työntekijän osoitteen luominen tai muuttaminen

Voit päivittää osoitteen **henkilöstöhallinnan** työtilassa. Noudata seuraavia ohjeita luodaksesi tai muuttaaksesi osoitetta:

1. Valitse **henkilöstöhallinnan** työtilassa **linkit** ja valitse sitten **työntekijät**.
2. Valitse työntekijä ja valitse sitten **Osoitteet**.
3. Valitse **Lisää** lisätäksesi osoitteen. Jos haluat päivittää aiemmin luotua osoitetta, valitse osoite listasta ja valitse sitten **Muokkaa**.
4. Kirjoita **Nimi tai kuvaus**.
5. Valitse **Tarkoitus** avattavasta luetteloruudusta ja valitse sitten osoitetyyppi.
6. Syötä **Maa/alue**.
7. Kirjoita **postinumero**.
8. Kirjoita **katuosoite**.
9. Kirjoita **paikkakunta**, **osavaltio** ja **alue**. Yleensä nämä kentät määritetään automaattisesti **Postinumero**-kentän perusteella.
10. Vaihtoehtoisesti voit valita ensisijaisen osoitteen **ensisijaiselle** kentälle. Vain yksi osoite voidaan merkitä ensisijaiseksi. Jos toinen osoite on jo merkitty ensisijaiseksi osoitteeksi, sinun on vahvistettava, että haluat käyttää tätä osoitetta ensisijaisena.
11. Vaihtoehtoisesti voit valita yksityisen osoitteen **yksityiselle** kentälle. Vain käyttäjät, joilla on nimenomainen oikeus tarkastella yksityisiä osoitetietoja, voivat tarkastella tätä osoitetta.
12. Valitse **OK**.
 
## <a name="create-a-future-change-for-an-address"></a>Osoitteen tulevan muutoksen luominen

Joissakin tapauksissa saatat haluta päivittää osoitteen muuttumaan tulevaisuudessa. Tämä on hyödyllistä esimerkiksi silloin, kun työntekijä muuttaa seuraavan kuukauden 15. päivänä.

1. Avaa **Hallitse osoitteita** -sivu valitsemalla **Lisää asetuksia > Lisäasetukset** mistä tahansa osoiteruudukosta.
2. Luo uusi osoite valitsemalla **Uusi**.
3. Voit kirjoittaa osoitteen tiedot.
4. Valitse **Yleinen**-pikavälilehti.
5. Valitse **voimaantulopäivämäärä**-kentässä uuden osoitteen voimaantulopäivämäärä.
6. Valitse **vanhentumispäivämäärä** -kentästä, milloin osoite ei enää ole voimassa.
7. Sulje sivut.

## <a name="view-and-monitor-address-changes"></a>Osoitemuutosten tarkasteleminen ja seuranta

Henkilöstöhallinnon henkilöstö voi tarkastella ja seurata osoitemuutoksia **henkilöstönhallinta**-työtilassa. Jos haluat tarkastella osoitteenmuutoksia, valitse **Henkilöstöhallinto**-ruutu **aloitussivulta**. Osoitteenmuutokset näkyvät ruudun oikeassa yläkulmassa. Osoitteen yläpuolella oleva numero ilmaisee, kuinka monta **osoitemuutosta** on tapahtunut **Henkilöstöhallinnon parametrit** -sivulla määritettyjen päivien määrän aikana. 

Kun valitset **osoitteenmuutokset**-ruudun, uusi sivu näyttää osoitteenmuutosten tiedot. Voit halutessasi valita **Sisällytä tulevia osoitemuutoksia** oikeassa yläkulmassa, jolloin osoitteenmuutokset tulevat näkyviin myöhemmin.

> [!NOTE]
> Jos haluat saada hälytyksen tai sähköpostiviestin näistä osoitemuutoksista, voit luoda uuden hälytyssäännön toimintoruudun **asetukset**-välilehteen. Lisätietoja hälytyssäännöistä on kohdassa [Hälytyssääntöjen luominen](../fin-ops-core/fin-ops/get-started/create-alerts.md).
>
> Jos haluat määrittää työnkulun osoitemuutoksille, voit valita hälytyssäännössä **Lähetä ulkoisesti** -vaihtoehdon ja Power Automate käynnistää sitten liiketoimintatapahtuman ja määrittää työnkulun. Lisätietoja on kohdassa [hälytykset liiketoimintatapahtumina](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).


[!INCLUDE[footer-include](../includes/footer-banner.md)]

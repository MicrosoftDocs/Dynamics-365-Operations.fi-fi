---
title: Luo työtilauksia ylläpitopyynnöistä
description: Tässä ohjeaiheessa kerrotaan, kuinka työtilauksia luodaan ylläpitopyynnöistä resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427134"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Luo työtilauksia ylläpitopyynnöistä

[!include [banner](../../includes/banner.md)]

 


Kun olet luonut ylläpitopyyntöjä, voit helposti muuntaa ne työtilauksiksi. Tässä aiheessa kuvataan nopein tapa käsitellä ylläpitopyyntöjä, päivittää useita ylläpitopyyntöjä samanaikaisesti ja luoda sitten työtilaus useille ylläpitopyynnöille samanaikaisesti. **Aktiiviset ylläpitopyynnöt** -tai **Omat toiminnallisen sijainnin ylläpitopyynnöt** -sivulla voit käsitellä myös yhtä ylläpitopyyntöä kerrallaan ja muuntaa yhdenylläpito pyynnön työtilaukseksi.

> [!NOTE]
> Jokainen ylläpitopyyntö voi liittyä vain yhteen työtilaukseen. Useita ylläpitopyyntöjä voidaan kuitenkin sisällyttää yhteen työtilaukseen, vaikka ylläpitopyynnöissä olisi eri resurssit.

1. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt**.
2. Ennen kuin voit luoda työtilauksen ylläpitopyynnöitä, sinun on valittava vähintään ylläpitotöiden tyyppi ylläpitopyyntöjä varten ja myös ylläpitotyön tyypin variantti ja ala, jos nämä tiedot ovat merkityksellisiä. Voit helposti päivittää ylläpitopyynnön tiedot ruudukkonäkymässä.
3. Kun olet valmis luomaan työtilauksen, valitse siihen sisällytettävät ylläpitopyynnöt.

    - Jos valitset useita ylläpitopyyntöjä, jotka muunnetaan työtilaukseksi, sekä **Resurssit**-kenttä että **Ylläpitotyön tyyppi** -kenttä on määritettävä ennen työtilauksen luomista.
    - Jos valitset yhden ylläpitopyynnön, joka muunnetaan työtilaukseksi, vain **Resurssit**-kenttä on määritettävä ennen työtilauksen luomista. Kun luot työtilauksen, voit kuitenkin valita ylläpitotyön tyypin (ja siihen liittyvän ylläpitotyön tyypin variantin ja alan, jos nämä tiedot ovat merkityksellisiä) **Luo työtilaus**  valintaikkunassa.

4. Valitse **Työtilaus**.
5. Määritä **Luo työtilaus** -valintaikkunassa kentät ja valitse sitten **OK**.

    Sanomapalkki saattaa ilmoittaa, että uusi työtilaus on luotu.

    Lisäksi kun luot ylläpitopyyntöön perustuvan työtilauksen ja jos ylläpitopyyntöön liittyvä resurssi sisältyy takuusopimukseen, sanomapalkki ilmoittaa sinulle takuusopimuksesta.

6. Valitse **Resurssien hallinta** \> **Yhteiset** \> **Työtilaukset** \> **Kaikki työtilaukset** ja avaa uusi työtilaus.

    ![Uuden työtilauksen avaaminen](media/05-manage-maintenance-requests.png)


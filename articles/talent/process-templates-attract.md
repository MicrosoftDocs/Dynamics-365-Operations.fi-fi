---
title: Prosessimallin luominen Attractissa
description: Tässä ohjeaiheessa on tietoja prosessimallin luomisesta Attractissa.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 694835d20e3401aaeb22aa19082a2cd0e3a0163a
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010703"
---
# <a name="create-a-process-template"></a>Luo prosessimalli

[!include [banner](includes/banner.md)]

*Työhönoton prosessimalli* sisältää kaikki tehtävät, joiden on sisällyttävä työn työhönottoprosessiin. Tässä ohjeaiheessa käsitellään prosessimallin elementtejä Microsoft Dynamics 365 Talent: Attractissa. Siinä käsitellään myös mallin luomista.

> [!NOTE]
> Mallin luonti sisältyy Attractin kattavaan työhönottolaajennukseen.

## <a name="template-management"></a>Mallien hallinta

Organisaatiot voit päättää, voivatko ryhmän jäsenet tai vain järjestelmänvalvojat luoda prosessimalleja Attractissa. Voit määrittää mallien hallinnan valitsemalla **Hallintakeskus** \> **Mallien hallinta**. Jos haluat, että ryhmän jäsenet luomat oman mallinsa, ota mallien hallinta käyttöön. Jos et ota mallien hallintaa käyttöön, vain järjestelmänvalvojat voivat luoda malleja.

## <a name="default-template"></a>Oletusmalli

Vain järjestelmänvalvojat voivat määrittää oletusmallin. Oletusmallia käytetään, jos mallia ei ole valittu työtä luotaessa. Määritä oletusmalli valitsemalla **Hallintakeskus** \> **Mallien hallinta**. Valitse oletusmalliksi valittavan mallin kortissa ensin ellipsipainike (**...**) ja sitten **Aseta oletukseksi**.

## <a name="create-a-process-template"></a>Prosessimallin luominen

Järjestelmänvalvojat, työhönottajat ja työhönottopäälliköt voivat luoda prosessimalleja. Prosessimalli koostuu *vaiheista* ja *tehtävistä*. Vaiheet ryhmittävät tehtävät yhteen. Oletusarvoisesti jokaisessa prosessimallissa on seuraavat tehtävät: potentiaalinen ehdokas, hakemus ja tarjous. Nämä tehtävät sisältävät vaiheet voidaan nimetä uudelleen. Voit lisätä muita vaiheita valitsemalla **+ Uusi vaihe**. Voit lisätä tehtäviä vaiheeseen joko vetämällä ne sopivaan vaiheeseen tai kaksoisnapsauttamalla tehtävää tehtäväluettelossa.

> [!NOTE]
> Ehdokkaat näkevät vaiheen nimet **Hakemuksen tila** -sivulla. Ota tämä huomioon, kun valitset vaiheiden nimiä.

Lisätietoja tehtävistä on kohdassa [Työhönottoprosessin tehtävät Attractissa](./activities-attract.md).

Luo työhönoton prosessimalli noudattamalla seuraavia ohjeita:

1. Valitse **Mallit**.
2. Valitse **Uusi**.
3. Kirjoita **Mallin nimi** -kenttään mallin nimi ja valitse sitten **Luo**.
4. Valitse **Valitse hyväksyntäprosessi** -luettelossa **Oletus**, jos haluat, että työ on aina hyväksyttävä.
5. Valitse, otetaanko potentiaaliset ehdokkaat käyttöön vai poistetaanko ne käytöstä.
6. Valinnainen: lisää tai poista vaiheita.

    - Lisää vaihe valitsemalla **+ Uusi vaihe**.
    - Poista vaihe pitämällä osoitinta vaiheen päällä ja valitsemalla esiin tuleva roskakoripainike.

        > [!NOTE]
        > Potentiaalinen vaihe-, Hakemus- ja Tarjous-vaiheita ei voi poistaa, mutta niiden nimi voidaan vaihtaa.

7. Valinnainen: lisää tai poista tehtäviä.

    - Voit lisätä tehtävän vetämällä sen oikeaan vaiheeseen oikealla olevassa tehtäväluettelossa. Vaihtoehtoisesti voit kaksoisnapsauttaa tehtävää ja valita sitten vaiheen, johon se lisätään.
    - Poista tehtävä laajentamalla se ja valitsemalla sitten roskakorikuvake tehtävän ylätunnisteessa.

8. Valitse **Tallenna**.

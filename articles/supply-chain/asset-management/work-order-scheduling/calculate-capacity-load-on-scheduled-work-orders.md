---
title: Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen
description: Tässä ohjeaiheessa selitetään, kuinka voit laskea kapasiteettikuormituksen ajoitetuille työtilauksille käyttöomaisuuden hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0c0dd1e306c54d3f99b86ad6f1816d5acabe6c18
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887156"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Ajoitettujen työtilausten kapasiteetin kuormituksen laskeminen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Voit laskea ajoitettujen työtilausten kapasiteetin kuormituksen, jolloin saat yleiskuvan resurssien työkuormituksesta tietyltä kaudelta. Voit tehdä laskelmia seuraavista resursseista: Kunnossapitotyöntekijät, työntekijäryhmät, työkalut ja resurssit.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Ajoitus** > **Kapasiteetin kuormitus**.

2. Valitse **Laske kapasiteetin kuormitus** -valinta ikkunan **Näytä**-kentästä laskettava kuormitustyyppi: "kapasiteetti", "varattu" tai "jäljellä oleva".

3. Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa on nolla.

4. Valitse resurssityypit, joille haluat laskea kapasiteetin kuormituksen, valitsemalla "kyllä" asiaankuuluvissa vaihtopainikkeissa: **Työntekijä**, **Ylläpitotyöntekijäryhmä**, **Työkalu**ja **Resurssi**.

5. Valitse aloituspäivämäärä laskennalle **Aloituspäivämäärä**-kentästä.

6. Valitse **Välityyppi**-kentästä laskutoimitusten väli: päivä, viikko, kuukausi tai vuosineljännes.

7. Lisää **Jakson frekvenssi** -kenttään, kuinka monta aikaväliä haluat laskea. Jos esimerkiksi olet valinnut aika välityypiksi "päivä" ja lisäät tähän kenttään numeron "5", aloituspäivämäärästä lasketaan viisi päivää eteenpäin.

8. Aloita laskenta valitsemalla **OK**.

Alla oleva kuva näyttää tuloksen, joka kattaa kolme viikkoa kuormitustyypistä "varattu".

![Kuva 1](media/08-work-order-scheduling.png)

>[!NOTE]
>Jos laskennalle valitaan kuormitustyypit "kapasiteetti" tai "jäljellä oleva", sama tulos tulee näkyviin, jos valitun kauden resursseille ei ole tehty varauksia.

Lisätietoja ylläpitoaikataulurivien kapasiteetin kuormituksen laskemisesta ja ei-ajoitetuista työtilauksista on kohdassa [Kapasiteetin kuormituksen laskeminen](../capacity-planning/calculate-capacity-load.md).


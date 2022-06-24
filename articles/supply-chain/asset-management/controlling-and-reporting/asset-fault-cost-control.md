---
title: Resurssivikojen kustannusten hallinta
description: Tässä artikkelissa kerrotaan resurssivikojen kustannushallinnasta resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 553b89a43b656669b7730b19898f3a5d81a3873a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889661"
---
# <a name="asset-fault-cost-control"></a>Resurssivikojen kustannusten hallinta

[!include [banner](../../includes/banner.md)]

 

Käyttöomaisuuden hallinnassa voit laskea käyttöomaisuuden vikamerkintöjen kustannukset, jolloin saat yleiskuvan todellisista kustannuksista verrattuna budjetin kustannuksiin. Todelliset kustannukset perustuvat kirjattuihin tapahtumiin. Päivämäärä on vikapäivämäärä, jolloin oire tallennettiin.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssin vika** > **Resurssivikojen kustannusten hallinta**.

2. Valitse **Resurssivikojen kustannusten hallinta** -valintaikkunassa laskennassa käytettävä taloushallinnon dimensioyhdistelmä, jos se on tarpeen.

4. Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa kustannus on nolla.

5. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia kustannushallinnan riveistä haluat liittyen toiminnallisiin sijainteihin. 

    Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintirakenne, kaikki toimintosijainnin vikakustannusten valvontarivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. 
    
    Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki resurssivikojen kustannushallintarivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

6. Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet, vikapäivämäärät ja virheiden syyt **Sisällytettävät tietueet** -pikavälilehdessä.

7. Aloita laskenta valitsemalla **OK**.

8. Valitse **Ryhmittely...**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut **Ryhmittely...**-painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

## <a name="example"></a>Esimerkki

Tässä esimerkissä esitetään resurssivikojen kustannushallinnan laskutoimituksista.

- **Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut kustannukset. 
- **Todelliset kustannukset** -kentässä näkyvät työtilausten kirjatut kustannukset. 
- **Sidottu kustannus** -kentässä näkyvät kokonaiskustannukset, joihin yritys on sitoutunut suhteessa työtilauksiin.

    ![Kuva 1.](media/05-controlling-and-reporting.png)

Lisätietoja vikojen määrittämisestä esitetään artikkelissa [Vikojen hallinta](../setup-for-work-orders/fault-management.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
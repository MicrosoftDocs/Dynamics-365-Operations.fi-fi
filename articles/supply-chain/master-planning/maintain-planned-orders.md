---
title: Ylläpidä suunniteltuja tilauksia
description: Tämä ohjeaihe sisältää suunniteltujen tilausten hallintaa käsitteleviä tietoja. Artikkelissa kuvataan, miten voit päivittää suunniteltujen tilausten tilan, vahvistaa ne ja suodattaa suunniteltuja tilauksia, joilla on sama tila kuin valitulla suunnitellulla tilauksella.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 039fce86ac9649989df1eaa6179c79dd98b8ae3f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967060"
---
# <a name="maintain-planned-orders"></a>Ylläpidä suunniteltuja tilauksia

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää suunniteltujen tilausten hallintaa käsitteleviä tietoja. Artikkelissa kuvataan, miten voit päivittää suunniteltujen tilausten tilan, vahvistaa ne ja suodattaa suunniteltuja tilauksia, joilla on sama tila kuin valitulla suunnitellulla tilauksella.

Voit hallita suunniteltuja tilauksia **Pääsuunnittelu**-työtilassa, **Suunniteltu tilaus** -luettelossa tai **Suunnitellut tuotantotilaukset**-, **Suunnitellut ostotilaukset**- ja **Suunniteltu siirto** -luettelossa. 

## <a name="planned-order-status"></a>Suunnitellun tilauksen tila
Voit seurata edistymistä **Tila**-kentässä. Käytettävissä ovat seuraavat arvot:

-   Kun pääsuunnittelu luo suunniteltuja tilauksia, suunniteltujen tilausten tilana on **Käsittelemätön**.
-   Jos et halua vahvistaa suunniteltua tilausta, voit asettaa sen tilaksi **Valmis**.
-   Jos haluat vahvistaa suunnitellun tilauksen, voit muuttaa tilaksi **Hyväksytty**. Pääsuunnittelu noudattaa suunniteltuja tilauksia, joiden tila on **Hyväksytty**, joten niitä ei muokata tai poisteta myöhemmän pääsuunnitteluajon aikana. Tämän saavuttamiseksi suunnittelulogiikka kopioi **hyväksytyt** suunnitellut tilaukset vanhasta suunnitelmaversiosta uuteen suunnitelmaversioon pääsuunnittelun aikana.

## <a name="firming-planned-orders"></a>Suunniteltujen tilausten vahvistaminen 
Vahvistettaessa suunniteltuja tilauksia luodaan todelliset tilaukset. Nämä tunnetaan myös nimellä *vapautetut* tai *avoimet* tilaukset. Kun suunniteltu tilaus on vahvistettu, se siirtyy kyseisen moduulin tilausosaan.

Voit valita kaksi vahvistusvaihtoehtoa **Suunnitellut tila ukset** -sivulta:

-   **Vahvista** – tämä vahvistaa yhden tai useita valittuja suunniteltuja tilauksia.
-   **Vahvista kaikki** – tämä vahvistaa suodattimen kaikki suunnitellut tilaukset. Käyttämällä **Vahvista kaikki** -toimintoa sinun ei tarvitse valita suunniteltua tilausta, kaikki suodattimen sisällä olevat suunnitellut tilaukset vahvistetaan. Tämä vaihtoehto voi olla hyödyllinen, jos olet vahvistamassa suunniteltujen tilausten suurta määrää.

> [!NOTE]
> Voit **vahvistushistoriassa** jäljittää suunnitellun tilauksen, joka on vahvistettu kohdassa **Suunnitellut tilaukset -lomake > Näytä > Vahvistushistoria**.

## <a name="parallelize-firming"></a>Rinnakkaisvahvistus
Jos aiot vahvistaa useita tilauksia samalla kertaa, suorituksen rinnakkaisuus voi parantaa ajoaikaa tai suorituskykyä. Tämä vaihtoehto on käytettävissä vahvistettaessa useita suunniteltuja tilauksia joko **Vahvista**- tai **Vahvista kaikki** -toiminnolla. Seuraavat parametrit ovat käytettävissä:

-   **Rinnakkainen vahvistus** – jos **Kyllä**, vahvistusprosessista tehdään rinnakkainen hyödyntämällä **Säikeiden määrä** -kohdassa määritettyä säikeiden määrää.
-   **Säikeiden määrä** – määrittää vahvistusprosessin rinnakkaisten säikeiden määrän. Parametri näkyy vain, kun **Rinnakkainen vahvistus** -arvoksi on määritetty **Kyllä.**

> [!NOTE]
> **Yhdenmukaista vahvistus** -vaihtoehto näkyy vain, kun vahvistumiseen on valittu useampi kuin yksi suunniteltu tilaus.

<a name="additional-resources"></a>Lisäresurssit
--------

[Pääsuunnitelmien yleiskatsaus](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
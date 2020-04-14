---
title: Määritä taloushallinnon dimensiot
description: Tässä tehtäväopastuksessa selvitetään yksikön tukeman taloushallinnon dimension ja mukautetun taloushallinnon dimension lisääminen.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138333"
---
# <a name="define-financial-dimensions"></a>Määritä taloushallinnon dimensiot

[!include [banner](../../includes/banner.md)]

Tässä tehtäväopastuksessa selvitetään yksikön tukeman taloushallinnon dimension ja mukautetun taloushallinnon dimension lisääminen.  Opastuksessa käytetään USMF-demoyritystä.


## <a name="create-an-entity-backed-financial-dimension"></a>Luo yksikön tukema taloushallinnon dimensio
1. Valitse **Siirtymisruutu > Moduulit > Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensiot**.
2. Valitse **Uusi**.
3. Valitse **Käytä arvoja** -lomakekentässä järjestelmän määrittämä yksikkö, johon taloushallinnon dimensio perustuu. 
4. Kirjoita **Dimension nimi** -kenttään taloushallinnon dimensiota kuvaava arvo. Nimi voi olla jokin muu kuin järjestelmän määrittämä yksikkö, mutta siinä ei saa olla välilyöntejä eikä erikoismerkkejä.
5. Valitse **Aktivoi**. Taloushallinnon dimension aktivointi päivittää taulun taloushallinnon dimension nimellä ja poistaa poistetut dimensiot. Voit antaa dimensioarvot ennen aktivoit taloushallinnon dimension aktivointia, mutta taloushallinnon dimensiota ei voi käyttää, ennen kuin se on aktivoitu.  
6. Valitse aktivointisanomassa **Sulje**.
7. Valitse **Aktivoi**. Dimension aktivointi voidaan ajoittaa suoritettavaksi erätyönä tiettynä päivämääränä ja kellonaikana.  
8. Valitse **toimintoruudussa** **Dimensioarvot**. Jotkin dimensioarvot ovat yrityskohtaisia. Voit tarkistaa, ovatko ne yrityskohtaisia sen perusteella, näkyykö yrityksen nimi dimensioarvoluettelossa.  

## <a name="create-a-custom-financial-dimension"></a>Luo mukautettu taloushallinnon dimensio
1. Sulje sivu.
2. Valitse **Uusi**.
3. Valitse **Käytä arvoja** -kentässä **Mukautettu dimensio**.
4. Kirjoita **Dimension nimi** -kenttään taloushallinnon dimensiota kuvaava arvo.
    - Nimi ei voi sisältää välilyöntejä eikä erikoismerkkejä.  
    - Voit määrittää myös tilipeitteen rajoittamaan dimensioarvoille annettavaa summaa ja tietojen tyyppiä.   
    - Voit syöttää merkkejä, jotka pysyvät samana jokaisessa dimensioarvossa, kuten kirjaimia tai yhdysviivan. Voit myös syöttää numeromerkkejä (#) ja et-merkkejä (&) paikkamerkkeinä kirjaimille ja numeroille, jotka muuttuvat aina, kun dimensioarvo luodaan. Käytä numeromerkkiä (#) numeron paikkamerkkinä ja et-merkkiä (&) kirjaimen paikkamerkkinä.  Esimerkki: jos haluat rajoittaa dimensioarvon kirjaimiin CC ja kolmeen numeroon, anna muotoilupeitteeksi CC-###.  
5. Valitse **Aktivoi**. Taloushallinnon dimension aktivointi päivittää taulun taloushallinnon dimension nimellä ja poistaa poistetut dimensiot. Voit antaa dimensioarvot ennen aktivoit taloushallinnon dimension aktivointia, mutta taloushallinnon dimensiota ei voi käyttää, ennen kuin se on aktivoitu.     
6. Valitse **Aktivoi**. Dimension aktivointi voidaan ajoittaa suoritettavaksi erätyönä tiettynä päivämääränä ja kellonaikana.      
7. Valitse **toimintoruudussa** **Dimensioarvot**.
8. Valitse **Uusi**.
9. Kirjoita **Dimensioarvo**-kenttään taloushallinnon dimension arvoa kuvaava nimi.
10. Kirjoita **Kuvaus**-kenttään taloushallinnon dimension arvon kuvaus.


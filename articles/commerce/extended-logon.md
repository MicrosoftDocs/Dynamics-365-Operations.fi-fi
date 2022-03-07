---
title: Jatketun sisäänkirjautumisen määrittäminen MPOS:ille ja Cloud POS:ille
description: Tässä aiheessa käsitellään Cloud POS:n ja Retail Modern POS:n (MPOS) laajennetun kirjautumisen määrittämistä.
author: boycezhu
ms.date: 09/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0cc3d3a3cadbc614e82b8cc7ae0b78406247cece
ms.sourcegitcommit: efcb853a68a77037cca23582d9f6f96ea573727a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7478668"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a>Laajennetun MPOS- ja pilvimyyntipistekirjautumisen määrittäminen

[!include [banner](includes/banner.md)]

Tässä aiheessa käsitellään Cloud POS:n ja Retail Modern POS:n (MPOS) laajennetun kirjautumisen määrittämistä.

## <a name="setting-up-extended-logon"></a>Jatketun sisäänkirjautumisen määrittäminen

Löydät viivakoodimuotojen asetukset kohdassa **Retail ja Commerce** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipisteen profiilit** &gt; **Toimintoprofiilit**. **Toiminnot**-pikavälilehti sisältää seuraavat jatkettuun sisäänkirjautumiseen liittyvät asetukset.

### <a name="staff-bar-code-logon"></a>Henkilökunnan viivakoodisisäänkirjautuminen

Kun **Henkilökunnan viivakoodisisäänkirjautuminen** -asetus on käytössä, työntekijät, joiden myyntipisteen sisäänkirjautumisen tunnistetietoihin on määritetty jatkettu sisäänkirjautuminen, voivat kirjautua sisään viivakoodin avulla.

### <a name="staff-bar-code-logon-requires-password"></a>Henkilökunnan viivakoodisisäänkirjautumisessa tarvitaan salasana

Kun **Henkilökunnan viivakoodisisäänkirjautumisessa tarvitaan salasana** -asetus on käytössä, henkilökunnan viivakoodisisäänkirjautuminen valitsee vain työntekijän, jolle on määritetty esitetty jatkettu sisäänkirjautuminen. Työntekijöiden on silti syötettävä salasanansa, kun tämä asetus on käytössä.

### <a name="staff-card-logon"></a>Henkilökunnan korttisisäänkirjautuminen

Kun **Henkilökunnan korttisisäänkirjautuminen** -asetus on käytössä, työntekijät, joiden myyntipisteen sisäänkirjautumisen tunnistetietoihin on määritetty jatkettu sisäänkirjautuminen, voivat kirjautua sisään magneettinauhan avulla.

### <a name="staff-card-logon-requires-password"></a>Henkilökunnan korttisisäänkirjautumisessa tarvitaan salasana

Kun **Henkilökunnan korttisisäänkirjautumisessa tarvitaan salasana** -asetus on käytössä, henkilökunnan korttisisäänkirjautuminen valitsee vain työntekijän, jolle on määritetty esitetty jatkettu sisäänkirjautuminen. Työntekijöiden on silti syötettävä salasanansa, kun tämä asetus on käytössä.

## <a name="assigning-an-extended-logon"></a>Jatketun sisäänkirjautumisen määrittäminen

Oletuksena vain päälliköt voivat määrittää työntekijöille jatketun sisäänkirjautumisen. Määritä laajennettu sisäänkirjautuminen, siirtymällä myyntipisteessä kohtaan **Jatkettu kirjautuminen**. Etsi sitten työntekijä syöttämällä hänen operaattorintunnus hakukenttään. Valitse työntekijä ja napsauta sitten **Määritä**. Lue tai skannaa työntekijälle määritettävä jatkettu sisäänkirjautuminen seuraavalla sivulla. Jos kortin luku tai skannaus luettiin onnistuneesti, **OK**-painike tulee näkyviin. Napsauta **OK** tallentaaksesi jatkettu sisäänkirjautuminen kyseiselle työntekijälle.

## <a name="deleting-an-extended-logon"></a>Jatketun sisäänkirjautumisen poistaminen

Poista työntekijälle määritetty jatkettu sisäänkirjautuminen etsimällä työntekijä **Jatkettu kirjautuminen** -toiminnon avulla. Valitse työntekijä ja napsauta sitten **Poista määritys**. Kaikki tälle käyttäjälle määritetyt jatketun kirjautumisen tunnistetiedot poistetaan.

## <a name="extending-extended-logon"></a>Jatketun kirjautumisen laajentaminen

Laajennettu kirjautuminen sallii valmiin yksilöivän tunnuksen koostuvan vain viidestä merkittävästä merkistä. Jos esimerkiksi määrität kaksi korttia, joiden tunnukset ovat "1234567" ja "1234578", molempien tunnukseksi katsotaan "12345". Voisit luoda laajennuksen tukemaan lisää merkkejä. Yksityiskohtaiset ohjeet [Laajennetun MPOS- ja pilvimyyntipistekirjautumisen laajentaminen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Kirjautumispalvelua voidaan laajentaa niin, että ne tukevat laajennettuja kirjautumislaitteita kuten käsiskannereita. Lisätietoja on POS-laajennettavuusdokumentaatiossa.

## <a name="using-extended-logon"></a>Jatketun sisäänkirjautumisen käyttäminen

Kun jatkettu sisäänkirjautuminen on määritetty ja työntekijälle on määritetty viivakoodi tai magneettinauha, työntekijän tarvitsee vain lukea tai skannata korttinsa myyntipisteen kirjautumissivulla. Jos tarvitaan myös salasana ennen kuin kirjautuminen voi jatkua, työntekijää kehotetaan syöttämään salasanansa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

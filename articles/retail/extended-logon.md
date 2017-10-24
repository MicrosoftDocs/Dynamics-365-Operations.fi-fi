---
title: "Jatketun sisäänkirjautumisen määrittäminen pilvimyyntipisteelle ja myyntipisteelle"
description: "Tässä aiheessa käsitellään Cloud POS:n ja Retail Modern POS:n (MPOS) laajennetun kirjautumisen määrittämistä."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e29aea4509dd323c295b02f289fbcfa46fab3392
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Jatketun sisäänkirjautumisen määrittäminen pilvimyyntipisteelle ja myyntipisteelle

[!include[banner](includes/banner.md)]


Tässä aiheessa käsitellään Cloud POS:n ja Retail Modern POS:n (MPOS) laajennetun kirjautumisen määrittämistä.

<a name="setting-up-extended-logon"></a>Jatketun sisäänkirjautumisen määrittäminen
=========================

Viivakoodimuotojen asetukset ovat **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipisteen profiilit** &gt; **Toimintoprofiilit**. **Toiminnot**-pikavälilehti sisältää seuraavat jatkettuun sisäänkirjautumiseen liittyvät asetukset.

### <a name="staff-bar-code-logon"></a>Henkilökunnan viivakoodisisäänkirjautuminen

Kun **Henkilökunnan viivakoodisisäänkirjautuminen** -asetus on käytössä, työntekijät, joiden myyntipisteen sisäänkirjautumisen tunnistetietoihin on määritetty jatkettu sisäänkirjautuminen, voivat kirjautua sisään viivakoodin avulla.

### <a name="staff-bar-code-logon-requires-password"></a>Henkilökunnan viivakoodisisäänkirjautumisessa tarvitaan salasana

Kun **Henkilökunnan viivakoodisisäänkirjautumisessa tarvitaan salasana** -asetus on käytössä, henkilökunnan viivakoodisisäänkirjautuminen valitsee vain työntekijän, jolle on määritetty esitetty jatkettu sisäänkirjautuminen. Työntekijöiden on silti syötettävä salasanansa, kun tämä asetus on käytössä.

### <a name="staff-card-logon"></a>Henkilökunnan korttisisäänkirjautuminen

Kun **Henkilökunnan korttisisäänkirjautuminen** -asetus on käytössä, työntekijät, joiden myyntipisteen sisäänkirjautumisen tunnistetietoihin on määritetty jatkettu sisäänkirjautuminen, voivat kirjautua sisään magneettinauhan avulla.

### <a name="staff-card-logon-requires-password"></a>Henkilökunnan korttisisäänkirjautumisessa tarvitaan salasana

Kun **Henkilökunnan korttisisäänkirjautumisessa tarvitaan salasana** -asetus on käytössä, henkilökunnan korttisisäänkirjautuminen valitsee vain työntekijän, jolle on määritetty esitetty jatkettu sisäänkirjautuminen. Työntekijöiden on silti syötettävä salasanansa, kun tämä asetus on käytössä.

<a name="assigning-an-extended-logon"></a>Jatketun sisäänkirjautumisen määrittäminen
===========================

Oletuksena vain päälliköt voivat määrittää työntekijöille jatketun sisäänkirjautumisen. Määritä laajennettu sisäänkirjautuminen, siirtymällä myyntipisteessä kohtaan **Jatkettu kirjautuminen**. Etsi sitten työntekijä syöttämällä hänen operaattorintunnus hakukenttään. Valitse työntekijä ja napsauta sitten **Määritä**. Lue tai skannaa työntekijälle määritettävä jatkettu sisäänkirjautuminen seuraavalla sivulla. Jos kortin luku tai skannaus luettiin onnistuneesti, **OK**-painike tulee näkyviin. Napsauta **OK** tallentaaksesi jatkettu sisäänkirjautuminen kyseiselle työntekijälle.

<a name="deleting-an-extended-logon"></a>Jatketun sisäänkirjautumisen poistaminen
==========================

Poista työntekijälle määritetty jatkettu sisäänkirjautuminen etsimällä työntekijä **Jatkettu kirjautuminen** -toiminnon avulla. Valitse työntekijä ja napsauta sitten **Poista määritys**. Kaikki tälle käyttäjälle määritetyt jatketun kirjautumisen tunnistetiedot poistetaan.

<a name="extending-extended-logon"></a>Jatketun kirjautumisen laajentaminen
========================

Kirjautumispalvelua voidaan laajentaa niin, että ne tukevat laajennettuja kirjautumislaitteita kuten käsiskannereita. Lisätietoja on POS-laajennettavuusdokumentaatiossa.

<a name="using-extended-logon"></a>Jatketun sisäänkirjautumisen käyttäminen
====================

Kun jatkettu sisäänkirjautuminen on määritetty ja työntekijälle on määritetty viivakoodi tai magneettinauha, työntekijän tarvitsee vain lukea tai skannata korttinsa myyntipisteen kirjautumissivulla. Jos tarvitaan myös salasana ennen kuin kirjautuminen voi jatkua, työntekijää kehotetaan syöttämään salasanansa.





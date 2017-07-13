---
title: "Jatketun sisäänkirjautumisen määrittäminen pilvimyyntipisteelle ja myyntipisteelle"
description: "Tässä aiheessa käsitellään Cloud POS:n ja Retail Modern POS:n (MPOS) laajennetun kirjautumisen määrittämistä."
author: josaw1
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 0b7e5ed451497aea1c2ce798af2b717705538d47
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017



---

# Jatketun sisäänkirjautumisen määrittäminen pilvimyyntipisteelle ja myyntipisteelle
<a id="set-up-extended-logon-functionality-for-cloud-pos-and-mpos" class="xliff"></a>

[!include[banner](includes/banner.md)]


Tässä aiheessa käsitellään Cloud POS:n ja Retail Modern POS:n (MPOS) laajennetun kirjautumisen määrittämistä.

Jatketun sisäänkirjautumisen määrittäminen
<a id="setting-up-extended-logon" class="xliff"></a>
=========================

Viivakoodimuotojen asetukset ovat **Vähittäismyynti** &gt; **Kanavan asetukset** &gt; **Myyntipisteen asetukset** &gt; **Myyntipisteen profiilit** &gt; **Toimintoprofiilit**. **Toiminnot**-pikavälilehti sisältää seuraavat jatkettuun sisäänkirjautumiseen liittyvät asetukset.

### Henkilökunnan viivakoodisisäänkirjautuminen
<a id="staff-bar-code-logon" class="xliff"></a>

Kun **Henkilökunnan viivakoodisisäänkirjautuminen** -asetus on käytössä, työntekijät, joiden myyntipisteen sisäänkirjautumisen tunnistetietoihin on määritetty jatkettu sisäänkirjautuminen, voivat kirjautua sisään viivakoodin avulla.

### Henkilökunnan viivakoodisisäänkirjautumisessa tarvitaan salasana
<a id="staff-bar-code-logon-requires-password" class="xliff"></a>

Kun **Henkilökunnan viivakoodisisäänkirjautumisessa tarvitaan salasana** -asetus on käytössä, henkilökunnan viivakoodisisäänkirjautuminen valitsee vain työntekijän, jolle on määritetty esitetty jatkettu sisäänkirjautuminen. Työntekijöiden on silti syötettävä salasanansa, kun tämä asetus on käytössä.

### Henkilökunnan korttisisäänkirjautuminen
<a id="staff-card-logon" class="xliff"></a>

Kun **Henkilökunnan korttisisäänkirjautuminen** -asetus on käytössä, työntekijät, joiden myyntipisteen sisäänkirjautumisen tunnistetietoihin on määritetty jatkettu sisäänkirjautuminen, voivat kirjautua sisään magneettinauhan avulla.

### Henkilökunnan korttisisäänkirjautumisessa tarvitaan salasana
<a id="staff-card-logon-requires-password" class="xliff"></a>

Kun **Henkilökunnan korttisisäänkirjautumisessa tarvitaan salasana** -asetus on käytössä, henkilökunnan korttisisäänkirjautuminen valitsee vain työntekijän, jolle on määritetty esitetty jatkettu sisäänkirjautuminen. Työntekijöiden on silti syötettävä salasanansa, kun tämä asetus on käytössä.

Jatketun sisäänkirjautumisen määrittäminen
<a id="assigning-an-extended-logon" class="xliff"></a>
===========================

Oletuksena vain päälliköt voivat määrittää työntekijöille jatketun sisäänkirjautumisen. Määritä laajennettu sisäänkirjautuminen, siirtymällä myyntipisteessä kohtaan **Jatkettu kirjautuminen**. Etsi sitten työntekijä syöttämällä hänen operaattorintunnus hakukenttään. Valitse työntekijä ja napsauta sitten **Määritä**. Lue tai skannaa työntekijälle määritettävä jatkettu sisäänkirjautuminen seuraavalla sivulla. Jos kortin luku tai skannaus luettiin onnistuneesti, **OK**-painike tulee näkyviin. Napsauta **OK** tallentaaksesi jatkettu sisäänkirjautuminen kyseiselle työntekijälle.

Jatketun sisäänkirjautumisen poistaminen
<a id="deleting-an-extended-logon" class="xliff"></a>
==========================

Poista työntekijälle määritetty jatkettu sisäänkirjautuminen etsimällä työntekijä **Jatkettu kirjautuminen** -toiminnon avulla. Valitse työntekijä ja napsauta sitten **Poista määritys**. Kaikki tälle käyttäjälle määritetyt jatketun kirjautumisen tunnistetiedot poistetaan.

Jatketun kirjautumisen laajentaminen
<a id="extending-extended-logon" class="xliff"></a>
========================

Kirjautumispalvelua voidaan laajentaa niin, että ne tukevat laajennettuja kirjautumislaitteita kuten käsiskannereita. Lisätietoja on POS-laajennettavuusdokumentaatiossa.

Jatketun sisäänkirjautumisen käyttäminen
<a id="using-extended-logon" class="xliff"></a>
====================

Kun jatkettu sisäänkirjautuminen on määritetty ja työntekijälle on määritetty viivakoodi tai magneettinauha, työntekijän tarvitsee vain lukea tai skannata korttinsa myyntipisteen kirjautumissivulla. Jos tarvitaan myös salasana ennen kuin kirjautuminen voi jatkua, työntekijää kehotetaan syöttämään salasanansa.





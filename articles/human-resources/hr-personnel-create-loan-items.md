---
title: Luo lainauskohteet
description: Lainan kohteet ovat tietueita, joiden avulla voit seurata fyysisiä yrityksen työntekijöille lainaamia kohteita, kuten puhelimia ja tietokoneita.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26bf5a83a6d25e99996ec4219c5fbbeed806e22d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693721"
---
# <a name="create-loan-items"></a>Luo lainauskohteet


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Lainan kohteet ovat tietueita, joiden avulla voit seurata fyysisiä yrityksen työntekijöille lainaamia kohteita, kuten puhelimia ja tietokoneita. Jokaisella fyysisellä kohteella on oltava vastaava lainan kohde. Jokaisessa lainan kohteen tietueessa tulisi kuvailla, mitä lainataan, kuka vastaa lainasta sekä aika (päivinä), jonka kohde voi olla lainassa. Voit luoda samalla useita lainan kohteita, kuten avaimia, kulkukortteja tai työpukuja. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-loan-types"></a>Lainatyyppien luominen
1. Valitse **Henkilöstöhallinto** > **Työntekijät** > **Lainan kohteet** > **Lainatyypit**.
2. Valitse **Uusi**.
3. Anna arvo **Lainatyyppi**-kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Määritä, kuinka monta päivää tätä lainatyyppiä olevat nimikkeet voivat olla myöhässä. 
6. Valitse **Tallenna**.
7. Sulje sivu.
8. Päivitä sivu.

## <a name="create-loan-items"></a>Luo lainauskohteet
1. Valitse **Henkilöstöhallinto** > **Työntekijät** > **Lainan kohteet** > **Lainan kohteet**.
2. Valitse **Luo lainauskohteet**.
3. Anna **Määrä**-kenttään numero.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Avaa haku valitsemalla **Lainatyyppi**-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Määritä, miten monta päivää kohde voi olla lainassa.
    * Lainatut välineet -sivun Suunniteltu palautus -kentän oletusarvo lasketaan lisäämällä kuluvaan päivämäärään tämä numero.  
9. Avaa haku valitsemalla **Vastuuhenkilö**-kentässä avattavan valikon painike.
10. Klikkaa **Valitse**.
11. Anna numero **Aloitusarvo**-kenttään.
12. Syötä numero **Väli**-kenttään.
13. Anna arvo **Muoto**-kenttään.
    * Jos lainan kohteen aloitusnumero on esimerkiksi 10, anna **Muoto**-kenttään kaksi numeromerkkiä.  
14. Valitse **OK**.
15. Päivitä sivu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Tehtävätallenteiden suojausdiagnostiikka
description: Tässä ohjeaiheessa on tietoja siitä, miten voidaan analysoida ja hallita tehtävän tallennukseen perustuvia käyttöoikeusvaatimuksia.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: cb4d544d8d74ad10432901381253f84ec9331ae7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745762"
---
# <a name="security-diagnostics-for-task-recordings"></a>Tehtävätallenteiden suojausdiagnostiikka

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Ennen aloittamista

Tässä ohjeaiheessa on tietoja siitä, miten voidaan analysoida ja hallita tehtävän tallennukseen perustuvia käyttöoikeusvaatimuksia. Ennen tämän ohjeaiheen vaiheiden suorittamista sinun on määritettävä analysoitavan liiketoimintaprosessin tehtävätallennus. Jos haluat tallentaa liiketoimintaprosessin, katso [Tehtävän tallennusresurssit](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Tehtävätallenteen suojauksenhallinta

1. Siirry kohtaan **Järjestelmänhallinta** > **Suojaus** > **Suojauksen vianmääritys tehtävätallennusta varten**.
2. Avaa tehtävätallennus sen sijainnista. Valitse **Avaa tästä tietokoneesta** tai **Avaa Lifecycle Servicesistä** ja valitse sitten **Sulje**.
3. Tämä avaa **Suojausvalikkovaihtoehdon tiedot** -sivun, jossa luetellaan prosessin edellyttämät suojausobjektit.

 > [!NOTE]
 > **Toiminto**- ja **Tuloste**-valikon vaihtoehdot eivät sisälly luetteloon.

4. Valitse käyttäjä **Käyttäjätunnus**-kentässä. Jos käyttäjällä ei ole joidenkin valikkovaihtoehtojen käyttöoikeuksia, **Puuttuvat käyttöoikeudet** -kentän arvoksi päivittyy **Kyllä**.
  
  ![Suojausvalikkokohteen tiedot -sivu](../media/Security-Menu-Item-Details.png)

5. Valitse **Lisää viite**, jos haluat nähdä luettelon suojausobjekteista, kuten rooleista, velvollisuuksista ja oikeuksista, jotka myöntävät puuttuvan käyttöoikeuden.
6. Valitse luettelosta suojausobjekti:

    - Jos **Rooli** on valittuna, valitse **Lisää rooli käyttäjään**. Tämä avaa **Määritä käyttäjät rooleihin** -sivun. Lisätietoja on [Käyttäjien määrittäminen käyttöoikeusrooleille](assign-users-security-roles.md) -sivulla.
    - Jos valittuna on **Velvollisuus**, valitse **Lisää velvollisuus rooliin**, valitse roolit, joihin vero lisätään, ja valitse sitten **OK**.
    - Jos valittuna on **Oikeus**, valitse **Lisää oikeus velvollisuuksiin**, valitse roolit, joihin vero lisätään, ja valitse sitten **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
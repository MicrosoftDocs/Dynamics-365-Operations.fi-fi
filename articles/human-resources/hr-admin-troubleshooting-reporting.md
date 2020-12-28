---
title: Raportointivaihtoehdot
description: Tässä artikkelissa kerrotaan, miten voidaan ratkaista ongelma, kun asiakas haluaa mukauttaa Microsoft Dynamics 365 Human Resources -raportteja tai luoda uusia raportteja.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51d84df5c3c29510e2742148b8c260a2cf402639
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527714"
---
# <a name="reporting-options"></a>Raportointivaihtoehdot

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Ympäristön tiedot**

Tämä ongelma koskee kaikkia ympäristöjä.

**Oire**

Asiakas halua mukauttaa Microsoft Dynamics 365 Human Resources -raportteja tai luoda uusia raportteja.

**Varasto-otto**

Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.

**Ratkaisu**

- Common Data Serviceen siirtyvät Human Resources -tiedot voidaan raportoida Power Apps Common Data Service -liittimen välityksellä Power BI Desktopiin. Huomaa, että Common Data Service sisältää Human Resources -tietojen alijoukon. Lisätietoja Power BI:stä ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen Power Apps Common Data Servicen avulla](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Sähköistä raportointia (ER) voi käyttää joissakin Human Resourcesin raporteissa. Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.
- Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Human Resourcesin Microsoft Office -integraation kautta tarjoamia erilaisia tietoyksiköitä.

**Pitkäaikainen ratkaisu**

Käyttöön tulee lisää Power BI -asetuksia, ja Common Data Serviceen tulee sisältymään entistä enemmän tietoja ja yksiköitä.

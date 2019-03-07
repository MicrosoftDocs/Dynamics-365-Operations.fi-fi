---
title: Talentin raportointivaihtoehdot
description: Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, kun asiakas haluaa mukauttaa Microsoft Dynamics 365 for Talent -raportteja tai luoda uusia raportteja.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304266"
---
# <a name="reporting-options-in-talent"></a>Talentin raportointiasetukset

[!include [banner](includes/banner.md)]

**Ympäristön tiedot**

Tämä ongelma koskee kaikkia ympäristöjä.

**Oire**

Asiakas halua mukauttaa Microsoft Dynamics 365 for Talent -raportteja tai luoda uusia raportteja.

**Varasto-otto**

Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.

**Ratkaisu**

- Sovellusten Common Data Serviceen siirtyvät Core HR -tiedot voidaan raportoida PowerApps CDS -liittimen välityksellä Power BI Desktopiin. Huomaa, että Common Data Service for Apps sisältää Core HR -tietojen alijoukon. Lisätietoja Power BI:stä ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen PowerApps Common Data Servicen avulla](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Sähköistä raportointia (ER) voi käyttää joissakin Talentin raporteissa. Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.
- Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Talentin Microsoft Office -integraation kautta tarjoamia erilaisia tietoyksiköitä.

**Pitkäaikainen ratkaisu**

Käyttöön tulee lisää Power BI -asetuksia, ja Common Data Service for Appsiin tulee sisältymään entistä enemmän tietoja ja yksiköitä.

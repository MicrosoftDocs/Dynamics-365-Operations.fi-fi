---
title: Talentin raportointivaihtoehdot
description: Tässä ohjeaiheessa kerrotaan, miten voidaan ratkaista ongelma, kun asiakas haluaa mukauttaa Microsoft Dynamics 365 Talent -raportteja tai luoda uusia raportteja.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897945"
---
# <a name="reporting-options-in-talent"></a>Talentin raportointiasetukset

**Ympäristön tiedot**

Tämä ongelma koskee kaikkia ympäristöjä.

**Oire**

Asiakas halua mukauttaa Microsoft Dynamics 365 Talent -raportteja tai luoda uusia raportteja.

**Varasto-otto**

Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.

**Ratkaisu**

- Common Data Serviceen siirtyvät Core HR -tiedot voidaan raportoida Power Apps Common Data Service -liittimen välityksellä Power BI Desktopiin. Huomaa, että Common Data Service sisältää Core HR -tietojen alijoukon. Lisätietoja Power BI:stä ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen Power Apps Common Data Servicen avulla](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Sähköistä raportointia (ER) voi käyttää joissakin Talentin raporteissa. Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.
- Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Talentin Microsoft Office -integraation kautta tarjoamia erilaisia tietoyksiköitä.

**Pitkäaikainen ratkaisu**

Käyttöön tulee lisää Power BI -asetuksia, ja Common Data Serviceen tulee sisältymään entistä enemmän tietoja ja yksiköitä.

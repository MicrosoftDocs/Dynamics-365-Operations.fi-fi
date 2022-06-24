---
title: Raportointivaihtoehdot
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin raporttien mukauttamisesta tai uusien raporttien luontia.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 421883d314fb27b4592e9be0455946ab3730fb1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856335"
---
# <a name="reporting-options"></a>Raportointivaihtoehdot


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**Ympäristön tiedot**

Tämä ongelma koskee kaikkia ympäristöjä.

**Oire**

Asiakas halua mukauttaa Microsoft Dynamics 365 Human Resources -raportteja tai luoda uusia raportteja.

**Varasto-otto**

Käyttäjä ei voi mukauttaa upotettuja Microsoft Power BI -raportteja.

**Ratkaisu**

- Dataverseen siirtyvät Human Resources -tiedot voidaan raportoida Power Apps Dataverse -liittimen välityksellä Power BI Desktopiin. Huomaa, että Dataverse sisältää Human Resources -tietojen alijoukon. Lisätietoja Power BI:stä ja koontinäytöistä on kohdassa [Power BI -raporttien ja koontinäyttöjen luominen Power Apps Common Data Servicen avulla](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Sähköistä raportointia (ER) voi käyttää joissakin Human Resourcesin raporteissa. Asiakaslähtöiset mukautukset voidaan tehdä ER-määritysvaihtoehtojen avulla.
- Tiedot voidaan viedä Microsoft Exceliin tai Microsoft Wordiin käyttämällä Human Resourcesin Microsoft Office -integraation kautta tarjoamia erilaisia tietoyksiköitä.

**Pitkäaikainen ratkaisu**

Käyttöön tulee lisää Power BI -asetuksia, ja Dataverseen tulee sisältymään entistä enemmän tietoja ja yksiköitä.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

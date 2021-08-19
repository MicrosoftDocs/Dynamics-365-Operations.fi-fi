---
title: Myyntitarjousten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 92b77c1b7de1f5c946e677c810c0d0e43427473e7ba26679df23f7663946dbc0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765391"
---
# <a name="troubleshoot-sales-quotations"></a>Myyntitarjousten vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>En saa muutettua palvelunimikkeen myyntitarjouksen myyntimäärää.

### <a name="issue-description"></a>Ongelman kuvaus

Jos yrität määrittää myyntimäärää (**SalesQty**) *Palvelu*-tyypin nimikkeelle myyntitarjouksen rivillä, saat viestin "Päivittäminen ei ole sallittua Määrä-kentän osalta".

### <a name="issue-resolution"></a>Ongelman ratkaisu

Et voi määrittää myyntimäärää tuotteille, jotka ovat palvelunimikkeitä. Jos esimerkiksi tarjoat nimikkeen asentamisen palvelua, määrän tallentaminen ei ole järkevää, koska fyysistä nimikettä ei ole. On vain palvelu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
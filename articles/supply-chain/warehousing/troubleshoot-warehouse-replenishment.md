---
title: Varaston täydennyksen vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varaston täydennystä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828079"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Varaston täydennyksen vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varaston täydennystä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Näyttöön tulee myös seuraava virhesanoma: "Työtä %1 ei voi vapauttaa, koska siinä on keskeneräinen täydennystyö.

### <a name="issue-description"></a>Ongelman kuvaus

Keräilytyö estetään riippuvaisen täydennystyön vuoksi.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Jos aaltokysynnän täydennystä käytettäessä keräilysijainti on täydennettävä lähdetilauksen kysynnän täyttämistä varten, järjestelmä luo sekä täydennystyön että keräilytyön. Se kuitenkin estää keräilytyön täydennystyön valmistumiseen saakka. Tämä on tarkoituksellista, sillä keräilysijainnissa ie ole riittävästi varastoa ellei täydennystyö valmistu. Suorita täydennystyö ja käsittele sitten keräilytyö.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
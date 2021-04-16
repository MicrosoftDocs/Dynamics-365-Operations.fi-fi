---
title: Varastotyön vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastotyötä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
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
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837438"
---
# <a name="troubleshoot-warehouse-work"></a>Varastotyön vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastotyötä käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Sarjanumeronimikkeitä sisältäviä rekisterikilpiä ei voi siirtää, jo tyhjä varasto-otto ja tyhjä vastaanotto sallitaan seurantadimensioryhmässä.

### <a name="issue-description"></a>Ongelman kuvaus

Rekisterikilpeä ei voi siirtää **Siirto**-valikkovaihtoehdolla, jos sarjanumeron asetuksena seurantadimensioryhmässä on *Tyhjä varasto-otto sallitaan* ja *Tyhjä vastaanotto sallitaan* ja jos samassa sijainnissa on useita rekisterikilpiä, joista osalla on sarjanumero ja osalla ei.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tämä ongelma korjataan muutoksilla, jotka otetaan käyttöön [KB 4571546:n](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) avulla. Näillä muutoksilla **Sarjanumero**-kenttää muuttuu valinnaiseksi, kun tyhjä vastaanotto ja tyhjä varasto-otto sallitaan.

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Varastonhallinnan mobiilisovelluksessa tukee seuraava virhesanoma siirtoja käsiteltäessä: Varaston omistaja %1 ei saa osallistua tähän prosessiin.

### <a name="issue-description"></a>Ongelman kuvaus

**Omistaja** seurantadimensio puuttuu, kun varastonhallinnan mobiilisovellusta käytetään siirtojen tekemiseen. Supply Chain Management -asiakasohjelman säännöllinen varastosiirtokirjauskansio näyttää toimivan odotetusti ja voidaan kirjat vain, jos **Omistaja**-dimensio on täytetty.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Tällä hetkellä varastonhallintaprosessit tukevat vain varastoa, jonka omistaja on yritys.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
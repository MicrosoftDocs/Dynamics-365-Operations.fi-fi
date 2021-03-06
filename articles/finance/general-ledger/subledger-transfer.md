---
title: Alareskontran siirto pääkirjanpitoon
description: Tässä ohjeaiheessa kuvataan, miten Microsoft Dynamics 365 Finance voi käsitellä kirjanpidon alakirjanpitoon liittyviä siirtoprosesseja.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897501"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Alareskontran siirto pääkirjanpitoon

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 Finance -ominaisuuksia, jotka liittyvät alareskontran kirjauskansiomerkintöjen erien siirtämisen sääntöihin.

Versioon 8.1 tehtiin muutoksia, joiden avulla voitiin siirtää sääntöjä. Tämä syrjäytti **Synkroninen**-vaihtoehdon. Lisätietoja on kohdassa [Finance and Operationsin poistetut tai vanhentuneet ominaisuudet](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Alireskontraerien siirtoon on käytettävissä seuraavat vaihtoehdot. 

 - Asynkroninen – Tämä vaihtoehto ajoittaa välittömästi alakirjanpidon kirjanpitomerkintöjen siirron kirjanpitoon. Kirjanpidon tosite kirjataan heti, kun resurssit ovat vapaana käsittelemään tätä pyyntöä palvelimessa. 

- Ajoitettu erä – Tämä vaihtoehto lisää kirjanpidon käsittelyjonoon siirrettävät alareskontran tapahtumat, joissa tapahtumat käsitellään tilauksen yhteydessä. Kirjanpidon tosite kirjataan ajoitettuna aikana, jos resurssit ovat vapaana käsittelemään tätä erätyötä palvelimessa. 
 
Versioon 10.0.8 tehtiin parannuksia, jotka parantavat Asynkroninen-vaihtoehdon suorituskykyä. Tämä toiminto on otettu käyttöön ominaisuuden nimen **alareskontran siirrossa kirjanpidon suorituskyvyn optimointiin**. 
 
Tämä toiminto tehostaa tietojen siirtämistä alareskontrasta pääkirjanpitoon. Se mahdollistaa prosessin tehokkuuden, ja se ryhmittelee yhdessä pienempien tapahtumien joukon siirrettäväksi. Tämä mahdollistaa eräpalvelimen tehokkaamman käytön. Tämä toiminto edellyttää, että eräpalvelin on määritetty, verkossa ja toimiva, jotta asynkroninen siirtovaihtoehto toimisi. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Alareskontran siirto pääkirjanpitoon
description: Tässä aiheessa kuvataan ominaisuuksia, jotka liittyvät alareskontran siirtoprosessiin pääkirjanpitoon.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 70a34fa1f4ee540d89ec05816e4065fb3e1df9ef
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727311"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Alareskontran siirto pääkirjanpitoon

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan ominaisuuksia, jotka liittyvät alareskontran kirjauskansiomerkintöjen erien siirtämisen sääntöihin.

Versioon 8.1 tehtiin muutoksia, joiden avulla voitiin siirtää sääntöjä. Tämä syrjäytti **Synkroninen**-vaihtoehdon. Lisätietoja on kohdassa [Finance and Operationsin poistetut tai vanhentuneet toiminnot](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Alareskontraerien siirtoon on käytettävissä seuraavat vaihtoehdot:

- **Asynkroninen** – Alareskontran kirjanpitomerkinnät pääkirjanpitoon ajoitetaan välittömästi. Pääkirjanpidon tosite kirjataan heti, kun resursseja on saatavilla käsittelemään pyyntöä palvelimessa.
- **Ajoitettu erä** – Alareskontran kirjanpitomerkinnät, jotka on siirrettävä, lisätään pääkirjanpidon käsittelyjonoon. Jonon merkinnät käsitellään siinä järjestyksessä, jossa ne vastaanotetaan. Kukin pääkirjanpidon tosite päivittää tilit ajoitettuna aikana, jos resursseja on saatavilla käsittelemään erätyötä palvelimessa.

Versioon 10.0.8 tehtiin parannuksia, jotka parantavat **Asynkroninen**-vaihtoehdon suorituskykyä. Tämä toiminto on otettu käyttöön ominaisuuden nimen **alareskontran siirrossa kirjanpidon suorituskyvyn optimointiin**.

Toiminto, jonka avulla alareskontran eriä siirretään asynkronisesti, helpottaa tietojen siirtämistä alareskontrasta pääkirjanpitoon. Toiminto käsittelee tapahtumat tehokkaammin ryhmittelemällä pienempien tapahtumien joukkoja ja siirtämällä tapahtumat ryhmiin. Kun tapahtumat on ryhmitelty, eräpalvelimen resursseja käytetään tehokkaammin.

Alareskontraerien asynkroninen siirto edellyttää, että eräpalvelin on asetettu, online-tilassa ja toimiva, koska erätehtävät luodaan välittömästi suoritettavaksi eräpalvelimella. Kun **Alareskontran siirto kirjanpidon suorituskyvyn optimointi** -ominaisuus on käytössä, **prosessin automaation** järjestelmän erätyön nimeltä **Prosessin automaation kyselyjärjestelmän työn** on myös oltava käytössä. Lisätietoja on kohdassa [Prosessin automatisointi](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Erätason tehokkuusmuutos käyttää yhtä toistuvaa erätyötä järjestelmän kaikille yrityksille. Suorituksen aikana luodaan uusi erätyö, joka käsittelee pakolliset tietueet, joita ei ole vielä siirretty. Lisäasetuksia voidaan ohjata järjestelmän hallinnan **Prosessiautomaatio**-sivulla. Tällä sivulla voit muokata taustaprosessia, muuttaa tiheyttä ja määrittää odotuskauden.

Lisätietoja prosessiautomaation määrittämisestä on kohdassa [Prosessiautomaatio](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

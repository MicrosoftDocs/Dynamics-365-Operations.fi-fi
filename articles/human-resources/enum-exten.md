---
title: Gender-perusvalintaluettelon laajennettavuus
description: Tässä artikkelissa on yhteenveto Gender-perusvalintaluettelon (enum) laajennettavuudesta .
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749312"
---
# <a name="gender-base-enum-extensibility"></a>Gender-perusvalintaluettelon laajennettavuus

**Gender**-valintaluettelo (enum) on nyt laajennettavissa. Tässä artikkelissa kuvataan muutokset, jotka sinun täytyy tehdä koodikantaan, jos aiot laajentaa **Gender**-valintaluetteloa.

## <a name="gender-vs-hcmpersongender"></a>Gender vs. HcmPersonGender

Sukupuoliarvoille on kaksi valintaluettelo:

- **Gender** (sovellusympäristö)
- **HcmPersonGender** (PersonnelManagement)

**Gender**-valintaluetteloa käytetään Microsoft Dynamics 365 Financessa, , kun taas **HcmPersonGender**-valintaluettelo koskee henkilöstöresurssien hallintajärjestelmää (HCM). Jos käytät henkilöstöresurssien hallintajärjestelmää ja teet muutoksia **Gender**-valintaluetteloon, sinun kannattaa tehdä samat muutokset myös **HcmPersonDer**-valintaluetteloon. Jos lisäät **Gender**-valintaluetteloon esimerkiksi arvon **Transsukupuolinen**, lisää **Transsukupuolinen**-arvo myös **HcmPersonGender**-valintaluetteloon.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (luokka)

Näiden kahden perusvalintaluettelon välistä käännöstä varten luotiin uusi **HcmPersonGenderTranformUtil**. Tämä luokka sisältää kaksi metodia: **convertGenderToHcmPersonGender** ja **convertHcmPersonGenderToGender**. Sinun tulisi luoda laajennus käyttämällä **komentoketjun** luokkaa tai **tapahtumien käsittelijöitä** ja laajentaa molemmat metodit kartoittaaksesi uudet arvot, jotka lisätään jompaankumpaan valintaluetteloon.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (luokka)

**PayrollStateWageTaxPrepDP**-luokka tarjoaa tietoja SQL Server Reporting Services (SSRS) -raportille **Payroll State Wage Tax Prep**. Yhdysvalloissa on käytettävissä kolme arvoa: **Male**, **Female** ja **Unspecified**. **populatePayrollStateWageTaxPrepTmp**-metodi sisältää switch-lauseen, jolla **HcmPersonGender**-valintaluettelon arvo kartoitetaan johonkin kolmeen seuraavasta kentästä: **IsMale**, **IsFemale** tai **IsUnspecifiedGender**. Switch-lauseen oletusarvo on **IsUnspecifiedGender**. Jos lisäät **HcmPersonGender**-valintaluetteloon arvoja, jotka haluat kartoittaa eri tavalla, sinun täytyy luoda laajennus käyttämällä **komentoketjun** luokkaa **populatePayrollStateWageTaxPrepTmp**-metodin sijasta muuttaaksesi arvoa tarvittavalla tavalla.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (luokka)

**smmOutlookSync_Contact**-integrointiluokka linkittää arvoja **Outlookista** ja **yhteyshenkilöistä**. **Outlook** tukee kolmea arvoa: **Male**, **Female** ja **Unspecified**. Luokassa on kaksi metodia, jotka auttavat sinua kartoittamaan **Genders**-arvot **OutlookGenders**-arvoihin. Oletusarvoinen metodi on **NonSpecific/UnSpecified**. Jos luot **Gender**-valintaluettelolle lisäarvoja, sinun tulisi luoda laajennus käyttämällä **komentoketjun** luokkaa molempien metodien tilalle ja kartoittaa arvot haluamallasi tavalla.

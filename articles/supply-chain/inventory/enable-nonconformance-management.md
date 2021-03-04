---
title: Määrityksistä poikkeamisen hallinta
description: Tässä artikkelissa kuvataan perusasetukset, jotka vaaditaan käytettäessä määrityksistä poikkeamista. Lisäasetukset on määritettävä, jos haluat käyttää laatutilauksia.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e66353dc3a4b4b7d9ff3c5f63bf3d4b0c70bda0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427146"
---
# <a name="nonconformance-management"></a>Määrityksistä poikkeamisen hallinta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan perusasetukset, jotka vaaditaan käytettäessä määrityksistä poikkeamista. Lisäasetukset on määritettävä, jos haluat käyttää laatutilauksia.

Voit ottaa määrityksistä poikkeamisen käyttöön seuraavien vaiheiden avulla:

1.  Määritä poikkeamiin liittyvät varaston ja varastonhallinnan parametrit.
    -   Määritä **Käytä laadunhallintaa** -vaihtoehdon arvoksi **Kyllä**.
    -   Syötä työn hinta paikallisena valuuttana **Tuntihinta**-kenttään. Tuntihintaa käytetään määrityksistä poikkeavien toimintojen kustannusten laskentaan. Tuntihinta ja lasketut kustannukset ovat määrityksistä poikkeamisen viitetietoja. Ne eivät vaikuta muihin toimintoihin.
    -   Käytä **Laadunhallinta** -välilehteä **Raportin asetukset** -sivulla, jotta voit määrittää tulostettavan asiakirjan tyypin. Voit tulostaa määrityksistä poikkeamisen raportin, määrityksistä poikkeamisen tunnisteen tai korjausraportin. Voit määrittää useita tietueita eri tiedostotyyppien raporttiin tulostamista varten tai sisäisten ja ulkoisten huomautusten tulostamista varten. On hyödyllistä käyttää **Asiakirjatyyppi**-sivua määritettäessä yksilöivä asiakirjatyyppi määrityksistä poikkeamiselle ja korjauksille. Voit haluta syöttää esimerkiksi määrityksistä poikkeamiseen liittyviä huomautuksia määrityksistä poikkeamisen yksilöivän asiakirjatyypin avulla. Tällöin yksilöivä asiakirjatyyppi määritetään raporttiasetuksissa.
    -   Syötä määrityksistä poikkeamisten ja korjausviitteiden numerosarjat.

2.  Ota käyttöön käyttäjien hyväksyntä määrityksistä poikkeamisille. Liitä **Käyttäjät**-sivun **Nimi**-kentässä työntekijä jokaiselle käyttäjälle, jonka on hyväksyttävä määrityksistä poikkeaminen. Järjestelmä käyttää työntekijöitä, jotka voivat muuttaa määrityksistä poikkeamisen tilan määrityksistä poikkeamisen historiatietojen seuraamista varten. Käyttäjät eivät voi hyväksyä määrityksistä poikkeamista, jos heille ei ole liitetty työntekijätunnusta.
3.  Määritä määrityksistä poikkeamisen liitettävät ongelmatyypit. Määritä **Ongelmatyypit**-sivulla luokitus laatuongelmille, joita kohdataan erityyppisissä määrityksistä poikkeamisen tyypeissä. Voit määrittää seuraavat määrityksistä poikkeamisen tyypit: **Sisäinen**, **Asiakas**, **Toimittaja**, **Palvelupyyntö**, **Tuotanto** ja **Oheistuotteen tuotanto**. Hyväksy yhdessä tai useassa määrityksistä poikkeamisen tyypissä käytettävä ongelmatyyppi **Määrityksistä poikkeamisen tyypit** -sivulla. Esimerkiksi vikakoodiin liittyvä ongelmatyyppiä saatetaan käyttää kaikissa määrityksistä poikkeamisen tyypeissä, kun taas asiakasvalituksiin liittyvää ongelmatyyppiä käytetään ehkä vain määrityksistä poikkeamisen **Asiakas**- ja **Palvelupyyntö**-tyypeissä.
4.  Määritä karanteenivyöhykkeet, jotka ohjaavat käsittelyä odottavaa viallista materiaalia. Määritä **Karanteenivyöhykkeet**-sivulla vyöhykkeet, jotka voidaan liittää määrityksistä poikkeamiseen. Tulostetussa määrityksistä poikkeamisen tunnuksessa näkyy määritetty karanteenivyöhyke ja käyttötiedot, jotka ohjaavat viallisen materiaalin käsittelyssä. Vyöhykkeet voivat vastata varastopaikkoja tai operatiivisia resursseja.
5.  Määritä korjauksiin liitettävät vianmääritystyypit. Määritä vianmääritystoimenpiteiden luokitus **Vianmääritystyypit**-sivulla. Korjaus ilmaisee hyväksytyn poikkeaman vianmääritystoimenpiteen ja sen tekijän. Se määrittää myös halutun ja suunnittelun valmistumispäivämäärän.
6.  Määritä muut määrityksistä poikkemisiin liitettävät toiminnot. Määritä **Toiminnot**-sivulla avulla luokitus hyväksytyn määrityksistä poikkeamisen käsittelyä varten. Kun liität määrityksistä poikkeamiseen toiminnon, voit myös määrittää yksityiskohtia tietoja, kuten tietoja liittyvästä materiaalista, työtunneista ja erilaisista toiminnon tekemiseen tarvittavista kuluista. Näiden tietojen avulla lasketaan toiminnon arvioitu kustannus. Tarkat tiedot ja arvioidut kustannukset on tarkoitettu viitetiedoiksi. Laatuun liittyvät toiminnot poikkeavat tuotantoreititystä varten määritettävistä toiminnoista.


<a name="additional-resources"></a>Lisäresurssit
--------

[Luo ja käsittele määritysten noudattaminen](tasks/create-process-non-conformance.md)

[Laadunhallintaprosessit](quality-management-processes.md)

[Määritä määrityksistä poikkeamisen hallinnan edellytykset](tasks/set-up-prerequisites-nonconformance-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
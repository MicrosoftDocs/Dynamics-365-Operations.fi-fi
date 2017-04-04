---
title: "Määrityksistä poikkeamisen hallinta"
description: "Tässä artikkelissa kuvataan perusasetukset, jotka vaaditaan käytettäessä määrityksistä poikkeamista. Lisäasetukset on määritettävä, jos haluat käyttää laatutilauksia."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 6f25e2930ff265df1f938cdf56e8a0f4993617af
ms.lasthandoff: 03/31/2017


---

# <a name="nonconformance-management"></a>Määrityksistä poikkeamisen hallinta

Tässä artikkelissa kuvataan perusasetukset, jotka vaaditaan käytettäessä määrityksistä poikkeamista. Lisäasetukset on määritettävä, jos haluat käyttää laatutilauksia. 

Voit ottaa määrityksistä poikkeamisen käyttöön seuraavien vaiheiden avulla:

1.  Määritä poikkeamiin liittyvät varaston ja varastonhallinnan parametrit.
    -   Määritä **Käytä laadunhallintaa** -vaihtoehdon arvoksi **Kyllä**.
    -   Syötä työn hinta paikallisena valuuttana **Tuntihinta**-kenttään. Tuntihintaa käytetään määrityksistä poikkeavien toimintojen kustannusten laskentaan. Tuntihinta ja lasketut kustannukset ovat määrityksistä poikkeamisen viitetietoja. Ne eivät vaikuta muihin toimintoihin.
    -   Käyttöä **Laadunhallinta** välilehti **raportin asetukset** sivulla, voit määrittää tulostettavat asiakirjan tyyppi. Voit tulostaa määrityksistä poikkeamisen raportin määrityksistä poikkeamisen tunniste tai korjausraportti. Voit määrittää useita tietueita eri tiedostotyyppien raporttiin tulostamista varten tai sisäisten ja ulkoisten huomautusten tulostamista varten. On hyödyllistä käyttää **Asiakirjatyyppi**-sivua määritettäessä yksilöivä asiakirjatyyppi määrityksistä poikkeamiselle ja korjauksille. Voit haluta syöttää esimerkiksi määrityksistä poikkeamiseen liittyviä huomautuksia määrityksistä poikkeamisen yksilöivän asiakirjatyypin avulla. Tällöin yksilöivä asiakirjatyyppi määritetään raporttiasetuksissa.
    -   Syötä määrityksistä poikkeamisten ja korjausviitteiden numerosarjat.

2.  Ota käyttöön käyttäjien hyväksyntä määrityksistä poikkeamisille. Liitä **Käyttäjät**-sivun **Nimi**-kentässä työntekijä jokaiselle käyttäjälle, jonka on hyväksyttävä määrityksistä poikkeaminen. Järjestelmä käyttää työntekijöitä, jotka voivat muuttaa määrityksistä poikkeamisen tilan määrityksistä poikkeamisen historiatietojen seuraamista varten. Käyttäjät eivät voi hyväksyä määrityksistä poikkeamista, jos heille ei ole liitetty työntekijätunnusta.
3.  Määritä määrityksistä poikkeamisen liitettävät ongelmatyypit. Määritä **Ongelmatyypit**-sivulla luokitus laatuongelmille, joita kohdataan erityyppisissä määrityksistä poikkeamisen tyypeissä. Voit määrittää seuraavat määrityksistä poikkeamisen tyypit: **Sisäinen**, **Asiakas**, **Toimittaja**, **Palvelupyyntö**, **Tuotanto** ja **Oheistuotteen tuotanto**. Hyväksy yhdessä tai useassa määrityksistä poikkeamisen tyypissä käytettävä ongelmatyyppi **Määrityksistä poikkeamisen tyypit** -sivulla. Esimerkiksi vikakoodiin liittyvä ongelmatyyppiä saatetaan käyttää kaikissa määrityksistä poikkeamisen tyypeissä, kun taas asiakasvalituksiin liittyvää ongelmatyyppiä käytetään ehkä vain määrityksistä poikkeamisen **Asiakas**- ja **Palvelupyyntö**-tyypeissä.
4.  Määritä karanteenivyöhykkeet, jotka ohjaavat käsittelyä odottavaa viallista materiaalia. Määritä **Karanteenivyöhykkeet**-sivulla vyöhykkeet, jotka voidaan liittää määrityksistä poikkeamiseen. Tulostetussa määrityksistä poikkeamisen tunnuksessa näkyy määritetty karanteenivyöhyke ja käyttötiedot, jotka ohjaavat viallisen materiaalin käsittelyssä. Vyöhykkeet voivat vastata varastopaikkoja tai operatiivisia resursseja.
5.  Määritä korjauksiin liitettävät vianmääritystyypit. Määritä vianmääritystoimenpiteiden luokitus **Vianmääritystyypit**-sivulla. Korjaus ilmaisee hyväksytyn poikkeaman vianmääritystoimenpiteen ja sen tekijän. Se määrittää myös halutun ja suunnittelun valmistumispäivämäärän.
6.  Määritä muut määrityksistä poikkemisiin liitettävät toiminnot. Määritä **Toiminnot**-sivulla avulla luokitus hyväksytyn määrityksistä poikkeamisen käsittelyä varten. Kun liität määrityksistä poikkeamiseen toiminnon, voit myös määrittää yksityiskohtia tietoja, kuten tietoja liittyvästä materiaalista, työtunneista ja erilaisista toiminnon tekemiseen tarvittavista kuluista. Näiden tietojen avulla lasketaan toiminnon arvioitu kustannus. Tarkat tiedot ja arvioidut kustannukset on tarkoitettu viitetiedoiksi. Laatuun liittyvät toiminnot poikkeavat tuotantoreititystä varten määritettävistä toiminnoista.


<a name="see-also"></a>Lisätietoja
--------

[Luo ja käsittele määrityksistä poikkeamisen (tehtävän guide)](https://ax.help.dynamics.com/en/wiki/create-and-process-a-nonconformance/)

[Quality management processes](quality-management-processes.md)

[Määritä määrityksistä poikkeamisen management (tehtävän guide) edellytykset](https://ax.help.dynamics.com/en/wiki/set-up-prequisites-for-nonconformance-management/)



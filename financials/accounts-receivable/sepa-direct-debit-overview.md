---
title: SEPA-suoraveloitusyhteenveto
description: "Yhtenäinen euromaksualue (SEPA) on Euroopan komission määrittämä, ja se määrää, että kaikki sähköiset maksut ovat kotimaisia, riippumatta henkilön, yrityksen tai organisaation ja pankin maasta tai alueesta. Kansallisten ja kansainvälisten maksujen välillä ei ole eroja. SEPA koostuu 28 Euroopan unionin (EU) jäsenvaltiosta sekä Islannista, Liechtensteinista, Norjasta, Sveitsistä, Monacosta ja San Marinosta. SEPA auttaa muodostamaan yksittäisen markkinan maksutapahtumille Euroopan talousalueella (ETA). SEPA:n odotetaan lopulta vähentävän sitä maksumuotojen määrää, joiden kanssa pankkien, liikeyritysten ja yksityishenkilöiden on toimittava."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f3b20b033fc701204cbb3f62468a421b3bdd6a80
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="sepa-direct-debit-overview"></a>SEPA-suoraveloitusyhteenveto

[!include[banner](../includes/banner.md)]


Yhtenäinen euromaksualue (SEPA) on Euroopan komission määrittämä, ja se määrää, että kaikki sähköiset maksut ovat kotimaisia, riippumatta henkilön, yrityksen tai organisaation ja pankin maasta tai alueesta. Kansallisten ja kansainvälisten maksujen välillä ei ole eroja. SEPA koostuu 28 Euroopan unionin (EU) jäsenvaltiosta sekä Islannista, Liechtensteinista, Norjasta, Sveitsistä, Monacosta ja San Marinosta. SEPA auttaa muodostamaan yksittäisen markkinan maksutapahtumille Euroopan talousalueella (ETA). SEPA:n odotetaan lopulta vähentävän sitä maksumuotojen määrää, joiden kanssa pankkien, liikeyritysten ja yksityishenkilöiden on toimittava.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>Mikä on SEPA-suoraveloitusten tavoite?
---------------------------------------

SEPA-suoraveloituksen avulla velkoja voi kerätä varansa asiakkaan pankkitililtä, edellyttäen, että asiakas on antanut velkojalle siihen kirjallisen toimivallan. Asiakas allekirjoittaa valtakirjan, joka antaa luotonantajalle valtuuden kerätä maksun ja neuvoo asiakkaan pankkia maksamaan maksukehotuksen. 

SEPA suorahyvitykset luovat ensimmäisen kerran maksuvälineen, jota voi käyttää sekä kansallisiin että rajojen yli tapahtuvien euromääräisissä suoraveloituksissa koko 32 SEPA-maiden/alueiden alueella. 

Käytettävissä on kaksi mallia: SEPA Core Direct Debit -malli ja SEPA Business to Business (B2B) Direct Debit -malli. Molemmat mallit käyttävät samaa muotoa.

## <a name="what-is-the-core-direct-debit-scheme"></a>Mikä on Core-suoraveloitusvaltakirjajärjestelmä?
SEPA Core Direct Debit Scheme on perusskeema. Sillä on seuraavat määritteet:
-   Varojen siirto suoritetaan euroina (vaikka pankkitilit sisältävät varoja muissa valuutoissa).
-   Sekä asiakkaalla että velkojalla tulee olla tili luottolaitoksessa, joka sijaitsee SEPA-alueella.
-   Asiakkaan on myönnettävä allekirjoitettu valtakirja luotonantajalle.
-   Valtakirjat vanhenevat 36 kuukautta viimeisen keräyksen jälkeen.
-   Velkojan on tallennettava valtakirjat niiden voimassaolon ajan ja vähintään 14 kuukautta viimeisen maksukehotuksen jälkeen.
-   Mallia voidaan käyttää yhteen (kertaluontoiseen) tai toistuvaan suoraveloitusten keräämiseen.
-   Asiakkailla on oikeus palautukseen ilman lisäkysymyksiä korkeintaan kahdeksan viikkoa tilin veloituksen jälkeen.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Mikä on Yritysten välinen SEPA-suoraveloitusvaltakirja?
SEPA B2B Direct Debit Scheme koskee yritysten välisiä tapahtumia ja perustuu SEPA Core Direct Debit -skeemaan. Tärkeimmät erot ovat:
-   SEPA B2B Direct Debit -skeemaa ei sallita, kun asiakas on yksityinen (kuluttaja).
-   Asiakkaalla ei ole oikeutta valtuutetun tapahtuman hyvitykseen.
-   Asiakkaan pankkien on varmistettava, että periminen on sallittua tarkistamalla perintä toimivallan tiedoilla. Asiakkaan pankkien ja asiakkaiden on suostuttava tarkastukseen, joka suoritetaan jokaiselle suoraveloitukselle.
-   Malli tarjoaa lyhyemmän ajanjakson suoraveloitusten julkaisemiseen ja vähentää palautusjaksoa.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Voinko käyttää COR1-mallia suoraveloitusvaltakirjoina?
Kyllä. Voit käyttää COR1-mallia SEPA-suoraveloitusvaltakirjaa Alankomaissa, Belgiassa, Espanjassa, Italiassa, Itävallassa, Ranskassa ja Saksassa. Malli tarjoaa velkojalle lyhyemmän ennakkoilmoitusjakson suoraveloituksen keräykseen.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Mitä ovat kansainväliset pankkitilinumerot (IBAN) and BIC-koodit?
International Bank Account Number (IBAN)-numeroa ja Bank Identifier Code (BIC) -koodia käytetään kaikkien tilien tunnistamiseen 32:ssa SEPA-maassa tai -alueella. Anna BIC SWIFT-koodi -kenttään ja IBAN-koodi IBAN-kenttään. Molemmat kentät sijaitsevat Pankkitilit-sivun Pankkitili-välilehden Lisätunnus-välilehdessä. Tämä koskee sekä laskuttajan pankkitiliä että asiakkaan pankkitiliä.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Missä annan velkojan tunnuksia (Suoraveloitus tunnukset)?
SEPA:ssa jokainen luotonantaja tunnistetaan yksilöivän tunnuksen avulla. Tämän tunnisteen avulla asiakas ja asiakkaan pankki voivat suodattaa jokaisen suoraveloituksen ja tämän jälkeen he voivat käsitellä tai hylätä suoraveloituksen asiakkaan ohjeiden mukaan. Laskuttajien on pyydettävä tätä tunnistetta pankkinsa kautta. Anna tämä tunniste yrityksen pankkitilin Suoraveloitustunnus-kentässä.

## <a name="what-are-mandates"></a>Mitä ovat suoraveloitusvaltakirjat?
Asiakas allekirjoittaa valtakirjan, joka antaa luotonantajalle valtuuden kerätä maksun ja neuvoo asiakkaan pankkia maksamaan maksukehotuksen. Asiakas voi antaa valtakirjan paperimuodossa tai sähköisesti. Oletusarvon mukaan valtakirja päättyy 36 kuukauden kuluttua siitä, kun viimeisin suoraveloitus on tehty.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Missä määritän SEPA suoraveloituksen tiedostomuoto (ISO 20022)?
SEPA-tietomuodot perustuvat ISO 20022 -viestistandardeihin. Valitse ensin Yleinen sähköinen raportointi -valintaruutu ja sitten SEPA-suoraveloitus vientimuodon määritykseksi, kun määrität ostoreskontran maksutavan. Käytät kyseistä maksutapaa, kun luot maksutiedoston asiakkaan maksukirjauskansion.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>Missä tiedostomuodoissa voin luoda SEPA-suoraveloituksen maksutiedostoja?
Voit luoda SEPA-suoraveloituksille sähköisiä maksutiedostoja seuraavissa muodoissa:
-   SEPA-suoraveloituksen maksutiedostojen PAIN.008.001.02 XML -tiedostomuoto Alankomaissa, Belgiassa, Espanjassa, Italiassa, Ranskassa ja Saksassa.
-   SEPA-suoraveloituksen maksutiedostojen PAIN.008.001.02 XML -tiedostomuoto Itävallassa ja PAIN.008.003.02 XML -tiedostomuoto Saksassa.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Miten hyvitykset ja palautukset toimivat SEPA-suoraanveloituksien kanssa?
Asiakkailla on tiettyjä oikeuksia palautuksiin molemmissa SEPA-suoraveloitusmalleissa. Asiakkaalla on oikeus peruuttaa kaikki valtuutetut tapahtumat kahdeksan viikon jakson aikana eräpäivän jälkeen ilman syytä. Luvattomien tapahtumien tapauksessa jaksoa laajennetaan 13 kuukautta määräpäivän jälkeen. Palautukset tehdyistä maksuista suoritetaan manuaalisesti Asiakastapahtumat -sivun Peruuta maksu -painikkeella.







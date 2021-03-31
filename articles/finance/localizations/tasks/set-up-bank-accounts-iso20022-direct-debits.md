---
title: Määritä asiakas ja asiakkaan pankkitilit ISO20022-suoraveloituksia varten
description: Tässä tehtävässä kerrotaan, miten ISO20022-suoraveloituksen maksutiedostossa vaadittavat asiakkaan pankkitili ja asiakkaan suoraveloitusvaltakirja määritetään.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d097caf3ad097e3107708c426ef668c70298c4f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209848"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Määritä asiakas ja asiakkaan pankkitilit ISO20022-suoraveloituksia varten

[!include [banner](../../includes/banner.md)]

Tässä tehtävässä kerrotaan, miten ISO20022-suoraveloituksen maksutiedostossa vaadittavat asiakkaan pankkitili ja asiakkaan suoraveloitusvaltakirja määritetään. Määritetyistä asiakkaan maksumuodoista riippuu, tarvitaanko asiakkaalle tai asiakkaan pankkitilille tähän ohjeeseen kuulumattomia lisätietoja ja mitä ko. lisätiedot ovat. 

Tämä tehtävä luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa.



Tämä on neljäs viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.


## <a name="set-up-a-customer-bank-account"></a>Asiakkaan pankkitilin määrittäminen
1. Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.
2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa Tili-kenttää arvolla DE-010.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Valitse toimintoruudussa Asiakas.
5. Valitse Pankkitilit.
6. Valitse Uusi.
7. Kirjoita arvo Pankkitili-kenttään.
8. Kirjoita arvo Nimi-kenttään.
    * Kirjoita esimerkiksi 'EUR bank'.  
9. Syötä tai valitse arvo Pankkiryhmät-kentässä.
10. Syötä arvon IBAN-kenttään.
    * Kirjoita esimerkiksi 'DE36200400000628808808'.  
11. Syötä arvo SWIFT-koodi-kenttään.
    * Esimerkki: Syötä COBADEFFXXX.  Huomaa, ettei SWIFT\BIC ole pakollinen monissa maksumuodoissa; se on kuitenkin suositeltavaa rekisteröidä pankkitilille.  
12. Valitse Tallenna.
13. Sulje sivu.
14. Valitse Muokkaa.
15. Laajenna Oletusmaksut-osa.
16. Syötä tai valitse arvo Pankkitili-kentässä.

## <a name="add-a-direct-debit-mandate"></a>Suoraveloitusvaltakirjan lisääminen
1. Laajenna Suoraveloitusvaltakirjat-osa.
2. ValitseLisää.
3. Syötä tai valitse arvo Laskuttajan pankkitili -kentässä.
    * Voit valita esimerkiksi arvon DEMF OPER.  
4. Syötä päivämäärä Allekirjoitus-kenttään.
5. Vahvista päivämäärän päivitys valitsemalla Kyllä.
6. Syötä tai valitse arvo Allekirjoitussijainti-kenttään.
7. Syötä numero Odotettu maksujen määrä -kenttään.
8. Valitse OK.
9. Valitse Tallenna.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
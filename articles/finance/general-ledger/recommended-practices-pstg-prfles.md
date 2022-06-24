---
title: Profiilien kirjaamisen suositellut käytännöt
description: Tässä artikkelissa kuvataan kirjausprofiilien määrittämisen suositellut käytännöt.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0e321f447b78b88c065e52bb7fad1c445e47b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849899"
---
# <a name="recommended-practices-for-posting-profiles"></a>Profiilien kirjaamisen suositellut käytännöt

On olemassa useita suositeltuja käytäntöjä, joita sinun tulee noudattaa, kun määrität kirjausprofiileja koko järjestelmässä. Tässä artikkelissa kuvataan erilaisia skenaarioita ja vastaavia suositeltuja käytäntöjä.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Älä salli manuaalista syöttölippua

**Päätilit**-sivulla **Älä salli manuaalista merkintää** -valintaruutu tulee valita mille tahansa päätilille, jota käytetään kirjausprofiilissa. Tämä asetus estää käyttäjiä kirjaamasta päiväkirjamerkintää manuaalisesti päätilille. Siksi se auttaa varmistamaan, että ala-arvo pysyy tasapainossa pääkirjan kanssa, ja auttaa helpottamaan täsmäytysprosessia.

Jos järjestelmän hallitsemaan ja automaattisesti kirjattavaan tiliin tarvitaan muutoksia, voit käyttää jotakin seuraavista tavoista:

- Luo toissijainen päätili, johon oikaisut voidaan kirjata. Käytä sitten summatiliä tai talousraporttien erityistä riviä tilien ryhmittelemiseen ja yhteensovittamiseen.
- Peruuta alkuperäiset tapahtumat asianmukaisessa ala-arvossa, tee tarvittavat korjaukset ja kirjaa sitten tapahtuma uudelleen saman alaryhmän kautta.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Kirjausprofiilien muuttaminen tapahtumien jälkeen

Jos muutat kirjausprofiilia tapahtumien olemassaolon jälkeen, täsmäytys voi epäonnistua ja alihuoltaja ja kirjanpito voivat olla loppumassa. Yleensä on suositeltavaa, että kirjausprofiilia **ei** muuteta tapahtumien jälkeen.

Jos muutoksia tarvitaan, varmista järjestelmän eheys seuraavien ohjeiden avulla:

- Tee muutokset jakson aikana.
- Tee muutokset, kun järjestelmässä ei tapahdu muita tapahtumia.
- Vahvista kirjanpito ja täsmäytä se alikirjanpitoon ennen muutosten tekemistä ja sen jälkeen.
- Kirjattuja tapahtumia ei päivitetä, jos muutat kirjausprofiilia. Harkitse tarkkaan, tarvitaanko muutoksia.
- Jos muutat varaston kirjausprofiileja, mieti, miten muutokset vaikuttavat käytettävissä olevaan varastoon ja kirjanpidon saldoihin. Jotkin muutokset saattavat edellyttää, että tuot varaston 0:aan (nolla), suljet varaston ja tuot varaston takaisin sisään muutosten jälkeen.
- Testaa muutokset aina muuhun kuin tuotantoympäristöön, ennen kuin teet ne tuotannossa.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Kirjausprofiilien muutosten valvonta tietokannan kirjaamisen avulla

Harkitse tietokannan kirjaamisen määrittämistä jokaiselle kirjausprofiilille ja kirjausta ohjaavia parametritaulukoille. Jos parametria tai profiilia muutetaan, sinulla on täydellinen valvontatietue siitä, mitä arvoa muutettiin, kuka muutti sitä, milloin sitä muutettiin ja mikä edellinen arvo oli. Nämä tiedot voivat olla kriittisiä täsmäytysprosessin aikana, ja tarkastaja saattaa tarvita liiteasiakirjoja.

Lisätietoja on kohdassa [Tietokantakirjauksen määrittäminen](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Käytä seuraavaa taulukkoa viitteenä tavallisille taulukoiden nimille, jotka liittyvät kirjausprofiileihin ja niihin liittyviin kirjausparametreihin.

| Sivun nimi | Siirtymispolku | Taulun nimi |
|-----------|-----------------|------------|
| Ostoreskontran parametrit | Ostoreskontra &gt; Asetukset &gt; Ostoreskontran parametrit | VendParm |
| Toimittajan kirjausprofiili | Ostoreskontra &gt; Asetukset &gt; Toimittajan kirjausprofiili | VendPosting |
| Kulujen koodi | Ostoreskontra &gt; Kulujen asetukset &gt; Kulukoodi tai Myyntireskontra &gt; Kulujen asetukset &gt; Kulukoodi | MarkupTable |
| Maksutavat | Ostoreskontra &gt; Maksun asetukset &gt; Maksutavat | VendPaymMode |
| Käteisalennukset | Ostoreskontra &gt; Maksuasetukset &gt; Käteisalennukset tai Myyntireskontra &gt; Maksuasetukset &gt; Käteisalennukset | CashDisc |
| Toimitusmaksu (Toimittaja) | Ostoreskontra &gt; Maksun asetukset &gt; Toimitusmaksu | VendPaymFee |
| Myyntireskontran parametrit | Myyntireskontra &gt; Asetukset &gt; Myyntireskontran parametrit | CustParm |
| Asiakkaan kirjausprofiilit | Myyntireskontra &gt; Asetukset &gt; Asiakkaan kirjausprofiilit | CustPosting |
| Maksutavat | Myyntireskontra &gt; Maksujen asetukset &gt; Maksutavat | CustPaymMode |
| Toimitusmaksu (Asiakas) | Myyntireskontra &gt; Maksujen asetukset &gt; Maksutavat | CustPaymFee |
| Resurssin vuokrausparametrit | Resurssin vuokraus &gt; Asetukset &gt; Resurssin vuokrausparametrit | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Pankkitilit | Maksuliikenteen hallinta &gt; Pankkitilit &gt; Pankkitilit | BankAccountsTable |
| Pankkitapahtumalajit | Maksuliikenteen hallinta &gt; Asetukset &gt; Pankin tapahtumatyypit | BankTransType |
| Eliminointisäännöt | Konsolidoinnit &gt; Asetukset &gt; Eliminointisääntö | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Kululuokat | Matkalaskut &gt; Asetukset &gt; Yleinen &gt; Kululuokat | ProjCategories |
| Käyttöomaisuuserien parametrit | Käyttöomaisuus &gt; Asetukset &gt; Käyttöomaisuuden parametrit | AssetParameters |
| Käyttöomaisuuserän kirjausprofiili | Käyttöomaisuus &gt; Asetukset &gt; Käyttöomaisuuden kirjausprofiilit | AssetLedgerAccounts<br>AssetDisposalParameters |
| Valuutan uudelleenarvostustilit | Kirjanpito &gt; Valuutat &gt; Ulkomaanvaluutan uudelleenarvostustilit | CurrencyLedgerGainLossAccount |
| Automaattisten tapahtumien tilit | Kirjanpito &gt; Kirjausmääritys &gt; Automaattisten tapahtumien tilit | LedgerSystemAccounts |
| Konsernin sisäinen laskenta | Kirjanpito &gt; Kirjausasetukset &gt; Konsernin sisäiset tilit | LedgerIntercompany |
| Tapahtuman kirjausmääritykset | Kirjanpito &gt; Kirjausasetukset &gt; Tapahtumien kirjausmääritykset | JournalizingDefinitionTrans |
| Kirjausmääritykset | Kirjanpito &gt; Kirjausasetukset &gt; Kirjausmääritykset | JournalizingDefintion |
| Kirjaus (Varasto) | Varastonhallinta &gt; Määritys &gt; Kirjaus &gt; Kirjaus | InventPosting |
| Kustannustyyppien koodit | Aiheutuneet kustannukset &gt; Kustannuslaskennan asetukset &gt; Kustannustyyppikoodit | ITMCostTypeTable |
| Resurssit | Tuotannonhallinta &gt; Asetukset &gt; Resurssit &gt; Resurssit | WrkCtrTable |
| Resurssiryhmät | Tuotannonhallinta &gt; Asetukset &gt; Resurssit &gt; Resurssiryhmät | WrkCtrResourceGroup |
| Tuotantoryhmät | Tuotannonhallinta &gt; Asetukset &gt; Tuotanto &gt; Tuotantoryhmät | ProdGroup |
| Kustannusluokat | Tuotannonohjaus &gt; Asetukset &gt; Reititykset &gt; Kustannusluokat | ProjCategory |
| Projektiryhmät | Projektinhallinta ja kirjanpito &gt; Asetukset &gt; Kirjaus &gt; Projektiryhmät | ProjGroup |
| Kirjanpidon asetukset (Projektit) | Projektinhallinta ja kirjanpito &gt; Asetukset &gt; Kirjaus &gt; Kirjanpidon asetukset | ProjPosting |
| Kulujen oletusvastatilit | Projektinhallinta ja kirjanpito &gt; Asetukset &gt; Kirjaukset &gt; Kulujen oletusvastatilit | ProjDefaultOffsetSetup |
| Ostohyvitysten hallinnan kirjausprofiilit | Ostohyvitysten hallinta &gt; Ostohyvitysten hallinnan kirjausasetukset &gt; Ostohyvityksen hallinnan kirjausprofiilit | TAMRebatePosting |
| Kirjanpidon kirjausryhmä (Vero) | Vero &gt; Asetukset &gt; Arvonlisävero &gt; Kirjanpidon kirjausryhmät | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Ryhmien muuttaminen tapahtumien jälkeen

Ole varovainen, kun muutat ryhmiä päätiedoissa. Jos määrität kirjausprofiilit käyttämällä ryhmiä, päätietueen ryhmän muuttaminen voi vaikuttaa negatiivisesti kykyä täsmäyttää kirjanpito alareskontraan. Voit esimerkiksi konfiguroida myyntitilauksen tuoton varaston kirjausprofiilin niin, että kutakin nimikeryhmää varten käytetään eri tuottotiliä. Jos muutat nimikkeelle määritettyä nimikeryhmää tapahtumien jälkeen, uusien tapahtumien tuotto kirjataan päivitetylle tilille. Ennen muutosta kirjatut tuotot säilyvät kuitenkin alkuperäisellä tilillä.

## <a name="testing-posting-profiles"></a>Kirjausprofiilien testaaminen

Ennen kuin siirryt liveen ja teet kirjausprofiileihin tai liittyviin parametreihin muutoksia tai lisäyksiä, jokainen skenaario on testattava. Jokaisen kirjaustyypin on vähintään testattava, jotta kirjaus toimii oikein. Suositeltava tapa on kuitenkin testata kaikki kirjausprofiilitapahtumat ja niiden yhdistelmät.

Oletetaan esimerkiksi, että asiakkaan kirjausprofiileja on kaksi, joista jokaisella on kolme asiakasryhmäkohtaista tietuetta. Tässä tapauksessa jokainen tapahtumalaji on testattava.

**Kirjausprofiilit:**

- **GEN**: Yleinen kirjausprofiili, jossa on yksi työntekijäryhmä, yksi asiakkaille ja yksi konsernin sisäinen. Kukin ryhmä viittaa eri myyntireskontran myyntitiliin.
- **PRE** – Ennakkomaksun kirjausprofiili, jossa on yksi tietue kaikille ennakkomaksuille, jotka osoittavat asiakkaan ennalta maksettuihin tileihin.

### <a name="testing-scenarios"></a>Testausskenaariot

- **Työntekijä**-ryhmän asiakkaan vapaatekstilasku, joka käyttää **GEN**-kirjausprofiilia
- **Työntekijä**-ryhmän asiakkaan vapaatekstilasku, joka käyttää **PRE**-kirjausprofiilia
- **Työntekijä**-ryhmän asiakkaan myyntitilauslasku, joka käyttää **GEN**-kirjausprofiilia
- **Työntekijä**-ryhmän asiakkaan myyntitilauslasku, joka käyttää **PRE**-kirjausprofiilia
- **Työntekijä**-ryhmän asiakkaan asiakasmaksun lasku, joka käyttää **GEN**-kirjausprofiilia
- **Työntekijä**-ryhmän asiakkaan asiakasmaksun lasku, joka käyttää **PRE**-kirjausprofiilia

Toista edellistä esimerkkiä varten kullekin asiakasryhmälle yksi testausskenaario ja toista jokainen testausskenaarioiden ryhmä kullekin lisätapahtumatyypille (esimerkiksi projektilaskut ja huollon hallinta).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Kirjanpidon yhteensovittaminen alareskontraan

Kirjanpito tulee täsmäyttää alareskontran kanssa jokaisella kaudella. Monissa moduuleissa on valmiita raportteja, joiden avulla täsmäytys voidaan tehdä. Voit kuitenkin kehittää mukautettuja raportteja tai laajentaa aiemmin luotuja raportteja raportointivaatimusten mukaisesti paikallisten vaatimuksiesi mukaan.

On suositeltavaa sulkea kausi ja täsmäyttää kaikki alareskontrat kirjanpitoon ennen lähetystä. Suosittelemme myös, että teet valevalmistelusiirron kaikista avoimista saldoista ja avoimista tapahtumista ennen ensimmäistä käyttöönottoa. Osana tätä prosessia on suoritettava täydellinen täsmäytys, jotta voidaan varmistaa, että saldojen ja avattavien tapahtumien siirto tasapainottaa vanhoja järjestelmiä ja että kaikki kirjanpidon alareskontran saldot ennen uusien tapahtumien luomista.

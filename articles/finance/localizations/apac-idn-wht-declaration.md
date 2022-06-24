---
title: Indonesian ennakonpidätysraportti
description: Tässä artikkelissa kerrotaan, miten Indonesian ennakonpidätysraportti konfiguroidaan ja muodostetaan.
author: sndray
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8acd9442ff4f0b7c19e3b4fcf211acce002e43d5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883178"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Indonesian ennakonpidätysraportti (ID-00005)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka määritetään ja luodaan PPH-ennakonpidätystiedosto, jota yritykset Indonesiassa käyttävät raportoimaan ennakonpidätystapahtumat e-Bupot-sovelluksessa.

Indonesian veroviranomainen (DGT) määrittää, että verovelvollisten yrittäjien (PKP), jotka on rekisteröity KPP Pratamassa tuloveron pidättäjiksi/kerääjiksi (PPh, artikla 23 ja/tai artikla 26) on sähköisesti ilmoitettava tuloveronpalautuksen artikloiden 23 ja 26 mukaan e-Bupot-sovelluksen avulla. 

- **Artikla 23** – Raportti sisältää kaikki toimittajien ennakonpidätystapahtumat, joissa ensisijaisen osoitteen maa-/aluekoodi on Indonesian koodi.
- **Artikla 26** – Raportti sisältää kaikki toimittajien ennakonpidätystapahtumat, joissa ensisijaisen osoitteen maa-/aluekoodi ei ole Indonesian koodi.

## <a name="prerequisites"></a>Edellytykset

- Yrityksen ensisijainen osoite on on oltava Indonesiassa.
- **Yleinen ennakonpidätys**-ominaisuus on otettava käyttöön **Ominaisuuksien hallinta** -työtilassa. Lisätietoja uusien ominaisuuksien käyttöönotosta on kohdassa [ominaisuuksien hallinnan yleiskuvaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="download-electronic-reporting-configurations"></a>Sähköisen raportoinnin konfiguraatioiden lataaminen

Tuontitiedoston luonti perustuu sähköisen raportoinnin (ER) konfiguraatioihin. Lisätietoja konfiguroitavan raportoinnin ominaisuuksista ja käsitteistä on kohdassa [Sähköinen raportointi](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Tuotanto- ja käyttäjähyväksyntätestausympäristöille on ohjeet aiheessa [Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Services -palveluista](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Voit luoda tuontitiedoston lataamalla seuraavat konfiguraatiot tietovarastosta:

- **Veroilmoitus model.version.93.xml** tai myöhempi versio
- **Veroilmoituksen malli mapping.version.93.153.xml** tai myöhempi versio
- **WHT PPh-skeeman tuonti (ID).version.93.14** tai myöhempi versio

## <a name="set-up-general-ledger-parameters"></a>Kirjanpidon parametrien määrittäminen

1. Valitse **Vero** \> **Asetukset** \> **Kirjanpitoparametrit**.
2. Valitse **Ennakonpidätys**-välilehden **Ennakonpidätysilmoituksen muodon määritys** -kentästä **WHT PPh -skeeman tuonti (ID)**. 
3. Kohdassa **Vero** \> **Asetukset** \> **Ennakonpidätys** \> **Ennakonpidätyksen tuottotyypit** voit määrittää **Kode Bukti Potong** -ennakonpidätystuottotyypin ja sitten määrittää koodit liittyviin nimikkeen ennakonpidätysryhmiin. Koodit ovat pakollisia, jotta integrointitiedosto voidaan luoda e-Bupot-sovelluksen avulla. 

## <a name="generate-the-withholding-import-file"></a>Ennakonpidätyksen tuontitiedoston muodostaminen

Tietyn kauden e-Bupot-tiedoston valmistelu- ja luontiprosessi perustuu Tilitä ja kirjaa maksun vero -työn aikana kirjattuihin ennakonpidätystapahtumiin.

Luo tiedosto noudattamalla seuraavia ohjeita.

1. Valitse **Vero** \> **Ilmoitukset** \> **Ennakonpidätys** \> **PPH-tuontitiedosto e-bupot 23 ja 26**.
2. Valitse raportille alku- ja loppupäivämäärä ja valitse sitten tilityskausi.
3. Syötä tapahtuman päivämäärä ja valitse **OK**.
4. Valitse kieli. Kaikki raportit on käännetty englanniksi (**en-us**) ja indonesiaksi (**id**).
5. Valitse yrityksen tyyppi ja kirjoita sitten tarkistus- ja asiakirjanumerot. 
6. Tarkista, onko esimies allekirjoittanut raportin. Nämä tiedot raportoidaan tiedostossa. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

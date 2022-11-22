---
title: Välitilitapahtumamaksujen määritykset ja käsittely
description: Tässä artikkelissa käsitellään asiakkaiden välitilimaksujen määrittämistä ja lisäämistä. Välitilimaksu on maksu, joka kirjataan kirjanpitoon kahdessa vaiheessa.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb563008f156e1bfa6e4e9a705e9170342719ce7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775165"
---
# <a name="set-up-and-process-bridged-payments"></a>Välitilitapahtumamaksujen määritykset ja käsittely

[!include [banner](../includes/banner.md)]

Välitilimaksu on maksu, joka kirjataan kirjanpitoon kahdessa vaiheessa. Tätä menetelmää käytetään yleensä silloin, kun maksutavaksi on määritetty **Pankki** ja tapahtumat on kirjattava pankkitilille vain, kun tapahtuma on tyhjentänyt pankin. Voit kuitenkin käyttää sitä myös kirjanpitotilinä. Tällöin summa siirretään päätililtä toiselle päätilille, kun välitilikirjaus käsitellään.

Voit luoda välitilimaksuja joko ostoreskontrasta tai myyntireskontrasta. Vaikka tässä artikkelissa kerrotaan, kuinka myyntisaamisten välitilikirjaus määritetään, ostoreskontratapahtumien vaiheet ovat samanlaiset.

## <a name="set-up-bridging-posting"></a>Välikirjausten määrittäminen

Jotta voit käyttää pääkirjauksia, sinun on määritettävä yksi tai useita maksutapoja niin, että ne käyttävät **Välitilikirjaus**-tapaa. Valitse sitten välitili.

1. **Myyntireskontra &gt; Maksun asetukset &gt; Maksutavat**.
2. Valitse aiemmin luotu maksutapa, jota varten välitilikirjaus otetaan käyttöön. Voit myös luoda uuden maksutavan.
3. Valitse **Välitilikirjaus**-valintaruutu.
4. Valitse **Välitili**-kentässä päätili, jonne maksut on kirjattava, ennen kuin ne tyhjennetään pankkitilille.
5. Sulje sivu.

## <a name="process-and-transfer-bridging-posting"></a>Prosessin ja siirron välitilikirjaus

Luo ja käsittele välitilikirjaus noudattamalla näitä ohjeita.

1. Valitse **Myyntireskontra &gt; Maksut &gt; Asiakkaan maksukirjauskansio**.
2. Luo kirjauskansio valitsemalla **Uusi**.
3. Valitse nimi **Nimi**-kentässä.
4. Lisää rivejä asiakkaan maksukirjauskansioon ja valitse tapa, joka on määritetty välitilikirjausta varten.
5. Kirjaa kirjauskansio. Tapahtumat kirjataan päätilille, jonka valitsit edellisen menettelyn **Välitili**-kentässä.

Kun tapahtumat ovat tyhjentäneet pankin ja haluat siirtää maksun päätililtä maksutavalle määritetylle maksutilille, toimi seuraavasti.

1. Siirry kohtaan **Kirjanpito &gt; Kirjauskansioviennit &gt; Yleiset kirjauskansiot**.
2. Luo kirjauskansio valitsemalla **Uusi**.
3. Valitse nimi **Nimi**-kentässä.
4. Avaa kirjauskansion tiedot valitsemalla **Rivit**.
5. Valitse **Toiminnot &gt; Valitse välitilitapahtumat**.
6. Merkitse kaikki tyhjennystiedot ja valitse sitten **Hyväksy**.
7. Kirjaa kirjauskansio.

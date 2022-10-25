---
title: Invoice Capture -ratkaisun yleiskatsaus
description: Tässä artikkelissa on tietoja Invoice Capture -ratkaisusta.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691162"
---
# <a name="invoice-capture-solution"></a>Invoice Capture -ratkaisu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä artikkelissa on tietoja Invoice Capture -ratkaisusta, joka luo automaattisesti toimittajan laskuja digitaalisten laskujen kuvista.

Ostoreskontraosasto hallitsee ja käsittelee vastaanotettujen tuotteiden ja palveluiden laskuja. Ostoreskontran kirjanpitäjä varmistaa toimittajan laskujen tiedot seuraavista syistä:

- Lisätyön välttäminen, jos oikaisut tai korjaukset ovat pakollisia kauden sulkemisen aikana
- Toimittajan maksujen maksaminen ajallaan ja taloudellisten tappioiden estäminen virheen tai petoksen vuoksi

OCR-tekstintunnistus on otettu viime vuosina yleisesti käyttöön eri toimialoilla. Nykyään on yleistä, että tulostetut tekstit digitalisoidaan. Tällöin digitaalinen muokkaus, haku, tilaa säästävä tallennus ja näyttäminen verkossa on mahdollista. Digitaalista tekstiä voidaan käyttää koneen prosesseissa, kuten kognitiivisessa laskemisessa, konekäännöksissä, teksti puheeksi -toiminnossa, tärkeissä tiedoissa ja tekstin louhimisessa.

Tekoälyteknologian kehittyminen on mahdollistanut uudet OCR-tekstintunnistusratkaisut, jotka lukevat erilaisia laskumuotoja eri toimittajilta melko itsenäisesti, ilman ihmisten toimia. Monet yritykset ovat todenneet, että ne voivat säästää työtä ja parantaa tarkkuutta käsittelemällä laskuja automaation avulla manuaalisen käsittelyn sijaan.

## <a name="system-landscape"></a>Järjestelmä – vaaka

Seuraavassa kuvassa näkyvät Invoice Capture -ratkaisun pääosat ja -vaiheet.

[![Invoice Capture -ratkaisun osat ja vaiheet.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Vaaditut roolit

Seuraavassa taulukossa näkyvät roolit, joita Invoice Capture -ratkaisun määrittäminen ja käyttäminen edellyttää.

| Rooli          | Toiminnot | Järjestelmät | Roolien nimet |
|---------------|---------|---------|-----------|
| Järjestelmänvalvoja | <ul><li>Määritä ympäristöt Microsoft Power Platformissa.</li><li>Näytä ratkaisut Microsoft Power Platformissa.</li><li>Määritä Dynamics 365:n ja AI Builderin väliset yhteydet.</li><li>Määritä Azure Data Lake Storage -sijainnit.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365 -järjestelmänvalvoja</li><li>Power Platformn järjestelmänvalvoja</li><li>Tallennustilan blob-objektin tietojen omistaja</li></ul> |
| Tekoälyn laatija      | <ul><li>Ylläpidä työnkulkuja.</li><li>Luo mukautettuja tekoälymalleja.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Harrastelijatekijät</li></ul> |
| Ostoreskontran käsittelijä      | <ul><li>Tarkista toimittajan laskun valmistelualue ja tee tarvittavat toiminnot.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Uusi ostoreskontran käsittelijän rooli Power Platformissa</li></ul> |
| Ostoreskontran käsittelijä      | <ul><li>Suorita päivittäisiä toimintoja ostoreskontran käsittelijänä.</li><li>Siirry toimittajan laskun valmistelualueelle.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Ostoreskontra-assistentti</li></ul> |
  
Lisätietoja Invoice Capture -ratkaisun asentamisesta on kohdassa [Invoice Capture -ratkaisun asentaminen](../accounts-payable/install-invoice-capture.md).  

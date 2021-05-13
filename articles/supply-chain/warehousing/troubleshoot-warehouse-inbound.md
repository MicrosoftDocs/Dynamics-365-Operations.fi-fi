---
title: Saapuvien varastotoimintojen vianmääritys
description: Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun saapuvia varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920984"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Saapuvien varastotoimintojen vianmääritys

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään sellaisten yleisten ongelmien korjaamista, joita voi esiintyä, kun saapuvia varastotoimintoja käytetään Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Seuraava virhesanoma avautui: Laatutilaus %1 on luotu. Klusteriprofiilia ei löytynyt. Tarkista konfiguraatio.

### <a name="issue-description"></a>Ongelman kuvaus

Tämä virhesanoma liittyy vastaanottoprosessiin, jossa laadunhallinta on otettu käyttöön. Ympäristön määritysten mukaan virhesanoman luovan tapahtuman lisätiedot voivat auttaa korjaamaan ongelman.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Tarkista ensimmäiseksi [klusterikeräilyn](set-up-cluster-picking.md) määritys ja varmista, että klusteriprofiilit on määritetty oikein. Et voi käyttää mobiililaitteen klusterikeräilyn valikkokohdetta, ellei klusteriprofiileja ole määritetty. Ympäristön mukaan on ehkä tarkistettava myös liittyvät määritykset.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Yhdistelmärekisterikilven vastaanottoa ei voi käyttää muussa kuin hyvityksen jakelukoodissa.

### <a name="issue-description"></a>Ongelman kuvaus

Kun jakelukoodin **Toiminto**-kentän määrityksenä on *Hyvitys* tai *Hävikki*, voit käyttää [Yhdistelmärekisterikilven vastaanotto](mixed-license-plate-receiving.md) -valikkovaihtoehtoa palautettujen nimikkeiden käsittelemiseen.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Tällä hetkellä yhdistelmärekisterikilven vastaanotossa tuetaan vain [jakelukoodeja](../service-management/set-up-disposition-codes.md), joissa **Toiminto**-kentän asetuksena on *Hyvitys* tai *Hävikki*.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Kun kausittainen tuotteen vastaanottojen päivitystehtävä suoritetaan, vahvistamattomat ostotilaukset vahvistetaan.

### <a name="issue-description"></a>Ongelman kuvaus

Kun olet suorittanut kausittaisen *Päivitä tuotteen vastaanotot* -tehtävän, järjestelmä vahvistaa automaattisesti vahvistamattomat ostotilaukset, joiden varastotapahtuman tila on *Rekisteröity*.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Uusi saapuvan kuorman käsittelyominaisuus *Kuormamäärien ylivastaanottaminen* korjaa tämän ongelman. Ota tämä ominaisuus käyttöön siirtymällä [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilaan ja ottamalla seuraavat ominaisuudet käyttöön (alla olevassa järjestyksessä):

1. Liitä ostotilauksen varastotapahtumat kuorman kanssa
1. Kuormamääriä vastaanotettu liikaa

Lisätietoja on kohdassa [Kirjattujen tuotemäärien kirjaaminen ostotilauksiin](inbound-load-handling.md#post-registered-quantities).

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Kun rekisteröin saapuvia tilauksia, näyttöön tulee seuraava virhesanoma: Määrä ei kelpaa.

### <a name="issue-description"></a>Ongelman kuvaus

Jos saapuvien tilausten rekisteröimiseen käytettävässä mobiililaitteen valikkokohteessa on määritetty **rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi *Käyttäjän määrittämä*, näkyviin tulee virhesanoma (Määrä ei kelpaa) etkä voi tehdä rekisteröintiä valmiiksi.

### <a name="issue-cause"></a>Ongelman syy

Kun *Käyttäjän määrittämä* -arvoa käytetään rekisterikilpien ryhmittelykäytäntönä, järjestelmä jakaa saapuvan varaston erillisiksi rekisterikilviksi, kuten yksikköjärjestysryhmä määrittää. Jos vastaanotettavan nimikkeen jäljittämiseen käytetään erä- tai sarjanumeroita, kunkin erän tai sarja määrät on määritettävä rekisteröityä rekisterikilpeä kohden. Jos rekisterikilvelle määritetty määrä ylittää määrän, joka on vielä vastaanotettava nykyisille dimensioille, näyttöön tulee virhesanoma.

### <a name="issue-resolution"></a>Ongelman ratkaisu

Kun rekisteröit nimikkeen käyttämällä kannettavan laitteen valikkonimikettä, jossa **Rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi on määritetty *Käyttäjän määrittämä*, järjestelmä saattaa edellyttää, että vahvistat tai määrität rekisterikilpinumerot, eränumerot tai sarjanumerot.

Järjestelmä näyttää rekisterikilven vahvistussivulla määrän, joka on varattu nykyiselle rekisterikilvelle. Järjestelmä näyttää erä- tai sarjavahvistussivuilla määrän, joka on edelleen vastaanotettava nykyiselle rekisterikilvelle. Siihen sisältyy myös kenttä, johon voit syöttää rekisteröitävän määrän tätä rekisterikilven ja erä- tai sarjanumeron yhdistelmää varten. Varmista tässä tapauksessa, että rekisterikilvelle rekisteröitävä määrä ei ylitä vielä vastaanotettavaa määrää.

Vaihtoehtoisesti, jos saapuvan tilauksen rekisteröinnissä luodaan liian monta rekisterikilpeä, **Rekisterikilpien ryhmittelykäytäntö** -kentän arvoksi voidaan muuttaa *Rekisterikilpien ryhmittely*, nimikkeelle voi määrittää uuden yksikköjärjestysryhmän tai yksikköjärjestysryhmän **Rekisterikilpien ryhmittely** -vaihtoehdon aktivointi voidaan poistaa käytöstä.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Verolaskelmien tuominen ja vieminen
description: Tässä artikkelissa on tietoja veron laskentapalvelun tuonti- ja vientitoiminnosta.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 9daee683763d7cb0eb9573497eb4e20cba9b1863
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855170"
---
# <a name="import-and-export-tax-calculations"></a>Verolaskelmien tuominen ja vieminen

Tässä artikkelissa on tietoja veron laskentapalvelun tuonti- ja vientitoiminnosta. Tämä toiminto auttaa varmistamaan joustavan ja tehokkaan konfigurointikokemuksen.

## <a name="import-and-export-tax-codes"></a>Verokoodien tuominen ja vieminen

### <a name="export-templates"></a>Vientimallit

1. Kirjaudu [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/) -palveluun.
2. Valitse **Globalisaatio-ominaisuudet** -työtilaan, valitse **Ominaisuudet** ja sitten **Verolaskenta**-ruutu.
3. Valitse aiemmin luotu ominaisuus tai [luo uusi ominaisuus](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Valitse **versioit**-ruudukosta **Muokkaa**.
5. Määritä **veron laskenta** -toiminnon sivulla [konfiguraatioversio](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Valitse **Verokoodit**-välilehdessä **Tuo**.
7. Lataa **TaxCodesTemplate.zip**-tiedosto valitsemalla **Vie verokoodimalli**.
8. Pura **TaxCodesTemplate.zip**. Verokoodimallit pakataan erikseen **laskennan alkuperä** -arvon mukaan.
9. Pura **By Net Amount.zip** -tiedosto, jos haluat saada seuraavat CSV-tiedostot:

    - **TaxCode.csv** – Syötä verokoodit.
    - **TaxLimit.csv** – Määritä kunkin verokoodin verorajat.
    - **TaxRate.csv** – Määritä kunkin verokoodin veroasteet.

> [!NOTE]
> Oletusarvon mukaan mallissa on käytettävissä mallien **näyte**-verokoodin merkinnät. Jos **malli**-verokoodia ei poisteta CSV-tiedostoista, se tuodaan toimintoon.

### <a name="import-tax-codes"></a>Tuo verokoodit

Tuo mallissa oleva **Malli**-verokoodi veron laskentatoimintoon noudattamalla seuraavia vaiheita.

1. Valitse RCS:n **Verolaskelma**-toiminto -sivun **Verokoodit**-välilehdestä **Tuo**.
2. Valitse **Selaa**, etsi ja valitse **TaxCode.csv**-tiedosto. Valitse sitten **Kohdetaulu**-kentästä **Verokoodi**.
3. Tuo verokoodi valitsemalla **OK**.
4. Etsi ja valitse **TaxRate.csv**-tiedosto. Valitse sitten **Kohdetaulu**-kentästä **Veroaste**.
5. Tuo veroaste valitsemalla **OK**.
6. Etsi ja valitse **TaxLimit.csv**-tiedosto. Valitse sitten **Kohdetaulu**-kentästä **Veroraja**.
7. Tuo veroraja valitsemalla **OK**.

Voit myös suoraan tuoda postinumerotiedoston, joka sisältää kaikki kolme CSV-tiedostoa. Näin voit tehdä tuonnin nopeasti ja helposti valmiiksi.

1. Valitse RCS:n **Verolaskelma**-toiminto -sivun **Verokoodit**-välilehdestä **Tuo**.
2. Valitse **Selaa**, etsi ja valitse **Net Amount.zip-tiedoston mukaan** ja valitse sitten **OK**.

### <a name="export-tax-codes"></a>Vie verokoodit

1. Valitse RCS:n **Verolaskelma**-toiminto -sivun **Verokoodit**-välilehdestä **Vie**.

    **Vienti**-painike on käytettävissä, kun **verokoodi**-ruudukossa on vähintään yksi verokoodi.

2. Valitse **OK**, jos haluat viedä kaikki ominaisuuden verokoodit postinumerotiedostossa.

> [!NOTE]
> Käytä vietyä tiedostoa mallina, kun haluat tuoda verokoodit vastaavaan toimintoon.

## <a name="import-and-export-applicability-rules"></a>Käytettävyyssääntöjen tuominen ja vieminen

### <a name="export-applicability-rules"></a>Soveltuvuussääntöjen vieminen

1. Kirjaudu sisään [RCS:ään](https://marketing.configure.global.dynamics.com/).
2. Valitse **Globalisaatio-ominaisuudet** -työtilaan, valitse **Ominaisuudet** ja sitten **Verolaskenta**-ruutu.
3. Valitse aiemmin luotu ominaisuus tai [luo uusi ominaisuus](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Valitse **versioit**-ruudukosta **Muokkaa**.
5. Määritä **veron laskenta** -toiminnon sivulla [konfiguraatioversio](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Valitse **Veroryhmän käytettävyys** -välilehden **Määritä veroryhmän käytettävyys** -ruudukon rivit.
7. Valitse **Avaa Microsoft Officessa** -painike ja valitse sitten **Veropalvelun dynaaminen käytettävyysmatriisi**.

    [![Vie käytettävyyssäännöt Microsoft Exceliin Veron laskenta -toimintosivulle.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Valitse **Lataa**, jos haluat viedä valitut rivit Microsoft Excel -laskentataulukkoon.

### <a name="import-applicability-rules"></a>Soveltuvuussääntöjen tuominen

Lataamasi Excel-laskentataulukon rakenne sisältää **Määritä veroryhmän käytettävyys** -ruudukon rakenteen. Voit lisätä uusia sääntöjä suoraan laskentataulukkoon. Kun olet valmis, voit tuoda uudet säännöt takaisin **Määritä veroryhmän käytettävyys** -ruudukkoon näiden vaiheiden mukaisesti.

1. Valitse ja kopioi Excel-laskentataulukossa tuotavat rivit.
2. Valitse RCS:n **Veron laskenta** -ominaisuussivun **Veroryhmän soveltuvuus** -välilehdeltä **Lisää**, jos haluat lisätä tyhjän tietueen **Määritä veroryhmän soveltuvuus** -ruudukon alaosaan.
3. Liitä kopioidut rivit ruudukkoon painamalla näppäinyhdistelmää **CTRL+V**.
4. Valitse **Tallenna**.

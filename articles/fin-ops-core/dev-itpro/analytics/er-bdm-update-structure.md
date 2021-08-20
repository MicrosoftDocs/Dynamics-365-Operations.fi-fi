---
title: Liiketoiminta-asiakirjan mallin rakenteen päivittäminen
description: Tässä aiheessa kerrotaan, kuinka liiketoiminta-asiakirjan malli voidaan päivittää käyttämällä Liiketoiminta-asiakirjan hallintaominaisuutta.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2f57e3f3a84a6e767755c69074bc194e90793e6edd79d0e07ae7449d45ec7539
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775283"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Liiketoiminta-asiakirjan mallin rakenteen päivittäminen 

[!include[banner](../includes/banner.md)]

Voit muokata liiketoiminta-asiakirjan mallia **Mallin rakenne** -ruudussa [Liiketoiminta-asiakirjan hallinta](er-business-document-management.md)  -mallin editorissa [lisäämällä uusia kenttiä](er-bdm-add-field-to-excel-template.md) malliin Microsoft Excelissä. Mallin rakenne päivitetään automaattisesti Dynamics 365 Finance -järjestelmässä, jotta se vastaa **Mallin rakenne** -ruudussa tehtyjä muutoksia.

Voit myös muokata mallia käyttämällä Office 365:n online-toimintoja. Voit esimerkiksi lisätä uuden nimetyn nimikkeen, kuten kuvan tai muodon, muokattavaan laskentataulukkoon. Tässä tapauksessa mallin rakennetta ei päivitetä automaattisesti Financeen, eikä lisäämäsi nimike näy **Mallin rakenne** -ruudussa. Voit päivittää mallin rakenteen Financessa manuaalisesti valitsemalla **Päivitä rakenne** mallieditorisivulla.

Saat lisätietoja tästä toiminnosta suorittamalla seuraavan esimerkin.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Esimerkki: liiketoiminta-asiakirjan mallin rakenteen päivittäminen

Tässä esimerkissä näytetään, miten järjestelmänvalvoja voi päivittää yrityksen liiketoiminta-asiakirjan mallin rakenteen sen jälkeen, kun mallia on muokattu Office Onlinessa. Seuraavissa osissa selitetään tarvittavat vaiheet.

### <a name="prepare-a-business-document-template-for-editing"></a>Liiketoiminta-asiakirjan mallin valmisteleminen muokkausta varten

Tee seuraavat toimet [Liiketoiminta-asiakirjan hallinnan yleiskatsaus](er-business-document-management.md) -kohdassa.

1. [Konfiguroi ER-parametrit](er-business-document-management.md#configure-er-parameters)
2. [Tuo ER-ratkaisut](er-business-document-management.md#import-er-solutions)
3. [Ota liiketoiminta-asiakirjojen hallinta käyttöön](er-business-document-management.md#enable-business-document-management)
4. [Konfiguroi parametrit](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Liiketoiminta -asiakirjan mallin muokkaaminen

1. Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.
2. Valitse **Luo uusi malli** -sivulla **Vapaan tekstin lasku (ER-näyte)(Excel)** -malli.
3. Valitse **Luo asiakirja**.
4. Syötä **Otsikko**-kenttään **FTI sample Litware**.
5. Luo uusi malli valitsemalla **OK**.

    > [!NOTE]
    > Jos et ole vielä kirjautunut sisään Office Onlineen, sinut [ohjataan Office 365 -kirjautumissivulle](er-business-document-management.md#frequently-asked-questions). Voit palata Finance-ympäristöön valitsemalla selaimen **Edellinen**-painikkeen.

    Uusi malli avataan muokkaamista varten mallieditori-sivun upotetussa Excel Online -ohjausobjektissa.

[![Liiketoiminta-asiakirjan hallinnan työtilan käyttäminen liiketoiminta-asiakirjan mallin muokkaamiseen.](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Muokattavan mallin nykyisen rakenteen tarkasteleminen

1. Valitse Excel Onlinessa valintanauhan **Näkymä**-välilehden **Näytä**-ryhmästä **Ruudukko**.
2. Valitse muokattavan mallin otsikon yläpuolella oleva suorakulmio. Tämä suorakulmio on kuva, jonka nimi on **rptHeaderCompLogo**.
3. Jos **Mallin rakenne** -ruutu on piilotettu, valitse **Näytä rakenne**.
4. Laajenna **Mallin rakenne** -ruudussa **Raportti \> Lasku \> rptHeader \> rptHeaderPart1**.
5. Huomaa, että Finances mallirakenteessa **rptHeaderCompLogo** -nimike esitetään **Report \> Invoice \> rptHeader \> rptHeaderPart1** -nimikkeen alielementtinä.

[![Liiketoiminta-asiakirjojen hallinnan työtilan käyttäminen muokattavan mallin nykyisen rakenteen tarkasteluun.](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Liiketoiminta-asiakirjan mallin rakenteen päivittäminen poistamalla kuva

1. Valitse Excel Onlinessa muokattavassa mallissa kuva **rptHeaderCompLogo**.
2. Poista valittu kuva muokattavana olevasta mallista noudattamalla jotakin seuraavista vaiheista:

    - Valitse **Delete**-näppäin näppäimistöltäsi.
    - Pidä kuvaa valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse **Leikkaa**.

    > [!NOTE]
    > The **rptHeaderCompLogo** nimike on edelleen Financen mallin rakenteessa, vaikka kuva ei enää sisälly Excel-malliin.

3. Valitsemalla **Päivitä rakenne** voit synkronoida Excelin ja Financen muokattavan mallin rakenteen.
4. Laajenna **Mallin rakenne** -ruudussa **Raportti \> Lasku \> rptHeader \> rptHeaderPart1**.
5. Huomaa, että **rptHeaderCompLogo**-nimike ei enää sisälly Financen mallirakenteeseen.

[![Liiketoiminta-asiakirjan hallinnan työtilan käyttäminen kuvan poistamiseen liiketoiminta-asiakirjan mallista.](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Liiketoiminta-asiakirjan mallin rakenteen päivittäminen lisäämällä kuva

1. Valitse Excel Onlinessa valintanauhan **Lisää**-välilehden **Kuvitus**-ryhmästä **Kuva**.
2. Valitse **Valitse tiedosto**, siirry lisättävän kuvan kohdalle, valitse se ja valitse sitten **OK**.
3. Valitse **Lisää**.
4. Siirrä uutta kuvaa, kunnes se on oikeassa paikassa. Excel nimeää kuvan oletusarvoisesti. Se voi esimerkiksi nimetä kuvan kuvaksi **Kuva 2**.
5. Valitsemalla **Päivitä rakenne** voit synkronoida Excelin ja Financen muokattavan mallin rakenteen.
6. Laajenna **Mallin rakenne** -ruudussa **Raportti \> Lasku \> rptHeader \> rptHeaderPart1**.
7. Huomaa, että uusi kuva sisältyy nyt nimikkeenä Financen mallirakenteeseen.

[![Liiketoiminta-asiakirjan hallinnan työtilan käyttäminen kuvan lisäämiseen liiketoiminta-asiakirjan malliin.](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Liittyvät linkit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)

[Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
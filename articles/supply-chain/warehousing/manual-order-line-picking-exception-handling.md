---
title: Myynti- ja siirtorivin keräilypoikkeusten manuaalinen käsitteleminen
description: Tässä artikkelissa kerrotaan, miten järjestelmänvalvojat voivat manuaalisesti kerätä varastotapahtumia (tai kumota niiden keräilyn) korjatakseen virheellisten myynti- ja siirtotilaustietojen aiheuttamia ongelmia.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403667"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Myynti- ja siirtorivin keräilypoikkeusten manuaalinen käsitteleminen

[!include [banner](../includes/banner.md)]

Myynti- ja siirtorivin keräilypoikkeusten manuaalinen käsitteleminen antaa järjestelmänvalvojille mahdollisuuden korjata ongelmia, jotka aiheutuvat virheellisistä myynti- ja siirtotilaustiedoista. Sen avulla luotetut käyttäjät voivat kerätä manuaalisesti myynti- ja siirtotilausriveihin liittyviä varastotapahtumia (tai kumota niiden keräilyn) samaan aikaan kun varaston prosessit ovat käynnissä.

Tässä kuvattuja toimintoja tulee käyttää vain, jos järjestelmä ei voi viimeistellä varastoprosessien pinoa tavalliseen tapaan. Oletusarvoisesti toimintoa voivat käyttää vain käyttäjät, joilla on järjestelmänvalvojan rooli. Oikeudet voi kuitenkin myöntää määrittämällä *Keräile myyntirivejä manuaalisesti* -oikeus halutuille rooleille.

## <a name="turn-on-this-feature-for-your-system"></a>Tämän ominaisuuden ottaminen käyttöön järjestelmällesi

Ennen tässä artikkelissa kuvattujen ominaisuuksien käyttöä ominaisuudet on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat tarkistaa [ominaisuuksien hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetusten avulla ominaisuuksien tilan ja ottaa ominaisuudet käyttöön. Ominaisuudet on lueteltu **Ominaisuuksien hallinta** -työtilassa käyttämällä seuraavia nimiä:

- *Manuaalinen myyntirivin keräyspalvelu järjestelmänvalvojalle tai vastaaville luotettaville käyttäjille*<br>(Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä.)
- *Manuaalinen siirtorivin keräyspalvelu järjestelmänvalvojalle tai vastaaville luotettaville käyttäjille*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Myynti- tai siirtotilausriveihin liittyvien tapahtumien korjaaminen

Seuraavien ohjeiden mukaan voit korjata tapahtumia, jotka liittyvät myynti- tai siirtotilausriveihin.

1. Noudata jotakin seuraavista vaiheista sen mukaan, minkä tyyppisen tilauksen haluat korjata:

    - Jos haluat korjata tapahtuman, joka liittyy myyntitilaukseen, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Puhdista \> Keräile myyntirivi manuaalisesti**.
    - Jos haluat korjata tapahtuman, joka liittyy siirtotilaukseen, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Puhdista \> Keräile siirtorivit manuaalisesti**.

1. Käytä **Keräile myyntirivit manuaalisesti**- tai **Keräile siirtorivit manuaalisesti** -sivulla ruudukon yläosassa oleva suodattimia, jos haluat löytää etsimäsi rivin. Valitse sitten kohdetilausrivi ruudukon yläosassa.
1. Käytä alaosan **Varastotapahtumat**-, **Kuormitusrivit**-, **Työrivit**- ja **Säilörivit**-välilehtiä tarkastellaksesi valitun rivin lisätietoja. Näiden välilehtien tiedot tarjoavat liittyvien varastoprosessien ja niiden tilojen yleiskatsauksen.
1. Valitse toimintoruudussa **Keräile**, jos haluat avata varastotapahtuman valitun tilausrivin **Keräile**-sivulla. Voit suorittaa tämän vaiheen myös varastoon jo vapautetuille tilausriveille. (Yleensä varastoon vapautettuja tilausrivejä ei voi avata **Keräile**-sivulla.)

    > [!NOTE]
    > Näyttöön voi tulla useita varoituksia, kun avaat **Keräile**-sivun. Tee toiminnot, joita näissä varoituksissa suositellaan. Voit saada esimerkiksi varoituksen tilausriveistä, jotka on linkitetty varastotyöhön. Tällaisessa tapauksessa kannattaa yrittää peruuttaa työ käyttämällä normaalia [työn peruutustoimintoa](cancel-warehouse-work.md) ennen manuaalista korjausta.

1. Valitse rivi **Tapahtumat**-ruudukossa ja valitse sitten **Lisää keräilyrivi** -kohta **Tapahtumat**-työkalurivillä.
1. Valittu rivi siirretään **Keräilyrivit**-ruudukkoon. Määritä tarvittavat arvot sarakkeille, joista puuttuu pakollisia tietoja. (Voit esimerkiksi määrittää sen sijainnin ja rekisterikilven nimikkeen keräilyä tai keräilyn kumoamista varten.)
1. Valitse **Vahvista kaikkien keräily** -kohta **Keräilyrivit**-työkalurivillä.

## <a name="correct-load-line-quantities"></a>Kuormitusrivien määrien korjaaminen

Seuraavia ohjeita noudattamalla voit korjata kuormitusrivin määrän.

1. Noudata jotakin seuraavista vaiheista sen mukaan, minkä tyyppisen tilauksen haluat korjata:

    - Jos haluat korjata tapahtuman, joka liittyy myyntitilaukseen, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Puhdista \> Keräile myyntirivi manuaalisesti**.
    - Jos haluat korjata tapahtuman, joka liittyy siirtotilaukseen, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Puhdista \> Keräile siirtorivit manuaalisesti**.

1. Käytä **Keräile myyntirivit manuaalisesti**- tai **Keräile siirtorivit manuaalisesti** -sivulla ruudukon yläosassa oleva suodattimia, jos haluat löytää etsimäsi rivin. Valitse sitten kohdetilausrivi ruudukon yläosassa.
1. Valitse **Kuormitusrivit**-välilehden alaosan työkalurivillä oleva **Korjaa kuormitusrivit manuaalisesti**.
1. Tarkista **Korjaa kuormitusrivit manuaalisesti** -sivun **Varastotapahtumat**-ruudukossa varastotapahtumat, jotka liittyvät valittuun kuormitusriviin.
1. Korjaa ruudukon yläosassa kuormitusrivien määrät tarvittaessa seuraavissa sarakkeissa:

    - **Luodun työn määrä**
    - **Kerätty määrä**
    - **Suunniteltu cross-docking-määrä**

    Järjestelmä vahvistaa näihin sarakkeisiin tehdyt muutokset.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

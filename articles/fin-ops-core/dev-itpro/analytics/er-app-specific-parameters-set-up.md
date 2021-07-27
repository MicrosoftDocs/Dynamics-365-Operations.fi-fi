---
title: ER-muodon parametrien määrittäminen yrityskohtaisesti
description: Tässä ohjeaiheessa käsitellään sähköisen raportoinnin (ER) muodon parametrien yrityskohtaista määrittämistä.
author: NickSelin
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9276a633d560bc95c868b9c12438b4f625ed169a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351887"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>ER-muodon parametrien määrittäminen yrityskohtaisesti

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Edellytykset

Näiden vaiheiden suorittaminen edellyttää, että ensin on suoritettu vaiheet kohdassa [ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja](er-app-specific-parameters-configure-format.md).

Tässä ohjeaiheessa olevien esimerkkien suorittaminen edellyttää jonkin seuraavan roolin Microsoft Dynamics 365 Finance (Finance) -käyttöoikeutta:

- Sähköisen raportoinnin kehittäjä
- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

## <a name="import-er-configurations"></a>ER-konfiguraatioiden tuominen

1.  Kirjaudu ympäristöön.
2.  Valitse oletuskoontinäytössä **Sähköinen raportointi**.
3.  Valitse **Raportointikonfiguraatiot**.
4.  Tuo Financen nykyiseen esiintymään määritykset, jotka vietiin RCS:stä (Regulatory Configuration Services) ohjeaiheen [ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja](er-app-specific-parameters-configure-format.md) vaiheiden suorittamisen aikana. Toimi seuraavien ohjeiden mukaisesti kussakin sähköisen raportoinnin (ER) määrityksessä ja suorita ohjeet seuraavassa järjestyksessä: tietomalli, mallimääritys ja muodot.

    1. Valitse **Exchange \> Lataa XML-tiedostosta**.
    2. Valitse tarvittava XML-muotoinen ER-määritystiedosto valitsemalla **Selaa**.
    3. Valitse **OK**.
    
    Seuraavassa kuvassa näkyy määritykset, jotka on oltava tehtyinä, kun olet valmis.

    ![Sähköisen raportoinnin konfiguroinnit -sivu.](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>DEMF-yrityksen parametrien määrittäminen

Voit määrittää ER-muodon sovelluskohtaiset parametrit ER-kehyksen avulla.

1.  Valitse **DEMF**-yritys.
2.  Valitse määrityspuussa muoto **LE-tietojen haun oppimismuoto**.
3.  Valitse toimintoruudussa **Konfiguroinnit**-välilehden **Sovelluskohtaiset parametrit**-ryhmässä **Määritys**.

    ![ER-sovelluskohtaiset parametrit -sivu.](./media/GER-AppSpecParms-LookupForm.PNG)
    
    Voit määrittää **Sovelluskohtaiset parametrit** -sivulla **LE-tietojen haun oppimismuoto** -muodon **Valitsin**-tietolähteen.
    
    Jos ER-perusmuodossa on useita **Haku**-tyyppisiä tietolähteitä, tietolähde on valittava **Haut**-pikavälilehdessä, ennen kuin tietolähteen sääntöjoukon määrittämisen voi aloittaa.
    
    Kullekin tietolähteelle voi määrittää erilliset säännöt jokaiselle valitun ER-muodon versiolle.
    
    Valitun ER-perusmuodon versiossa käytettävissä oleva haun kaikkien tietolähteiden koko sääntöjoukko muodostaa ER-muodon sovelluskohtaiset parametrit.

4.  Valitse ER-muodon versio **1.1.1**.
5.  Valitse **Ehdot**-pikavälilehdessä **Lisää**.
6.  Avaa haku valitsemalla uuden tietueen **Koodi**-kentässä avattavan valikon nuoli.

    Haku tuloksena on verotuskoodien luettelo valintaa varten. ER-perusmuodossa määritetty **Model.Data.Tax**-tietolähde palauttaa tämän luettelon. Koska tässä tietolähteessä on **Nimi**-kenttä, kunkin verokoodin nimi näkyy haussa.

    ![ER-sovelluskohtaiset parametrit -sivu.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  Valitse **VAT19**-verokoodi.
8.  Avaa haku valitsemalla uuden tietueen **Haun tulos** -kentässä avattavan valikon nuoli. Haun tuloksena on TaxationLevel-muodon luetteloinnin arvoluettelo valintaa varten.

    Huomaa, että jos sen käyttäjän ensisijaiseksi kieleksi on valittu suomi, jona olet kirjautunut sisään, haun arvojen otsikot ovat suomeksi, mikäli ne on käännetty ER-perusmuodossa. Jos lisäksi haun tietolähteen otsikko on käännetty, kyseinen otsikko näkyy käyttäjän ensisijaisella kielellä **Haku**-valintalehdessä.

    ![ER-sovelluskohtaiset parametrit -sivu.](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  Valitse **Normaali verotus** -arvo.

    Tämän tietueen lisääminen määrittää seuraavan säännön: aina kun **Valitsin**-haun tietolähdettä pyydetään ja **VAT19**-verokoodi välitetään argumenttina, **Normaali verotus** palautetaan pyydettynä verotustasona.

10. Valitse **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Koodi**-kentässä **InVAT19**-verokoodi.
    2. Valitse **Haun tulos** -kentässä **Normaali verotus** -arvo.
    
11. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Koodi**-kentässä **VAT7**-verokoodi.
    2. Valitse **Haun tulos** -kentässä **Alennettu verotus** -arvo.
    
12. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Koodi**-kentässä **InVAT7**-verokoodi.
    2. Valitse **Haun tulos** -kentässä **Alennettu verotus** -arvo.
    
13. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Koodi**-kentässä **THIRD**-verokoodi.
    2. Valitse **Haun tulos** -kentässä **Ei verotusta** -arvo.
    
14. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Koodi**-kentässä **InVAT0**-verokoodi.
    2. Valitse **Haun tulos** -kentässä **Ei verotusta** -arvo.
    
15. Valitse uudelleen **Lisää** ja toimi sitten seuraavasti:

    1. Valitse **Koodi**-kentässä **\*Ei tyhjä\*** -vaihtoehto.
    2. Valitse **Haun tulos** -kentässä **Muu**-arvo.
    
    Tämän viimeisen tietueen lisääminen määrittää seuraavan säännön: aina kun argumenttina välitetty verokoodi ei vastaa mitään edellisistä säännöistä, haun tietolähde palauttaa **Muu**-arvon pyydettynä verotustasona.

    ![ER-sovelluskohtaiset parametrit -sivu.](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. Valitse **Tila**-kentässä **Valmis**.

    Kun suoritat ER-muodon version, jonka tilana on joko **Valmis** tai **Jaettu**, tämän sääntöjoukon tilan on oltava **Valmis**. Muussa tapauksessa ER-perusmuodon suoritus keskeytyy, kun muoto yrittää ladata tietoja tästä sääntöjoukosta, kun **Valitsin**-haun tietolähdettä suoritetaan.
    
    Kun suoritan ER-muodon version, jonka tila on **Luonnos**, ER-perusmuoto voi käyttää tätä sääntöjoukkoa riippumatta siitä, mikä sen tila on.
    
17. Valitse **Tallenna**.
18. Sulje **Sovelluskohtaiset parametrit** -sivu.

## <a name="run-the-er-format-in-the-demf-company"></a>ER-muodon suorittaminen DEMF-yrityksessä

1.  Valitse määrityspuussa muoto **LE-tietojen haun oppimismuoto**.
2.  Valitse toimintoruudussa **Suorita**.
3.  Valitse avautuvassa valintaikkunassa **OK**.
4.  Lataa muodostuva raportti ja tallenna se paikallisesti.

    Huomaa, että muodostetussa raportissa **InVAT7**-verokoodin yhteenveto on **Alennettu**-tasolla sekä **VAT19**- ja **InVA19**-verokoodien yhteenvedot **Normaali**-tasolla. Yrityskohtaisen sääntöjoukon määritys määrittää tämän toiminnan.
    
5.  Valitse **Vero \> Välilliset verot \> Arvonlisävero \> Arvonlisäverokoodit**.
6.  Valitse **InVAT7**-verokoodi.
7.  Valitse toimintoruudun **Arvonlisäverokoodi**-välilehden **Kyselyt**-ryhmässä **Kirjattu arvonlisävero**. Voit sitten tarkastella tietoja veroarvosta ja käytetystä verokoodikohtaisesta veroprosentista.

    ![Kirjattu arvonlisävero -sivu.](./media/GER-AppSpecParms-Statement.PNG)

8.  Sulje Kirjattu arvonlisävero -sivu.

## <a name="set-up-parameters-for-the-usmf-company"></a>USMF-yrityksen parametrien määrittäminen

1.  Valitse **USMF**-yritys.
2.  Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
3.  Laajenna määrityspuussa **Model to learn parameterized calls**, laajenna **Parametrisoitujen kutsujen oppimismuoto** ja valitse **LE-tietojen haun oppimismuoto** -muoto.
4.  Valitse toimintoruudussa **Konfiguroinnit**-välilehden **Sovelluskohtaiset parametrit**-ryhmässä **Määritys**.
5.  Valitse valitun ER-muodon versio **1.1.1**.
6.  Valitse **Ehdot**-pikavälilehdessä **Lisää**.
7.  Avaa haku valitsemalla uuden tietueen **Koodi**-kentässä avattavan valikon nuoli.

    Haun tuloksena on nyt **USMF**-yritysveron verokoodiluettelo, josta valinta tehdään.

    ![ER-sovelluskohtaiset parametrit -sivu.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  Valitse **EXEMPT**-verokoodi.
9.  Valitse uuden tietuen **Haun tulos** -kentässä **Ei verotusta** -arvo.
10. Valitse **Lisää** uudelleen.
11. Valitse uuden tietueen **Koodi**-kentässä **\*Ei tyhjä\*** -vaihtoehto.
12. Valitse uuden tietuen **Haun tulos** -kentässä **Normaali verotus** -arvo.
13. Valitse **Tila**-kentässä **Valmis**.
14. Valitse **Tallenna**.

    ![ER-sovelluskohtaiset parametrit -sivu.](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. Sulje **Sovelluskohtaiset parametrit** -sivu.

## <a name="run-the-er-format-in-the-usmf-company"></a>ER-muodon suorittaminen USMF-yrityksessä

1.  Valitse määrityspuussa muoto **LE-tietojen haun oppimismuoto**.
2.  Valitse toimintoruudussa **Suorita**.
3.  Valitse avautuvassa valintaikkunassa **OK**.
4.  Lataa muodostuva raportti ja tallenna se paikallisesti.

    Huomaa, että muodostetussa raportissa on nyt käytetty uudelleen samaa ER-muotoa eri yrityksessä ilman, että ER-muotoa olisi säädetty.

## <a name="reuse-legal-entitydependent-parameters"></a>Yrityskohtaisten parametrien käyttäminen uudelleen

### <a name="export-parameters"></a>Vientiparametrit

1.  Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.
2.  Valitse **Raportointikonfiguraatiot**.
3.  Valitse määrityspuussa muoto **LE-tietojen haun oppimismuoto**.
4.  Valitse toimintoruudussa **Konfiguroinnit**-välilehden **Sovelluskohtaiset parametrit**-ryhmässä **Määritys**.
5.  Valitse ER-muodon versio **1.1.1**.
6.  Valitse toimintoruudussa **Vie**.
7.  Lataa muodostuva tiedosto ja tallenna se paikallisesti.

    Määritetty sovelluskohtaisten parametrien joukko on nyt viety XML-tiedostona.

### <a name="import-parameters"></a>Tuontiparametrit

1.  Valitse ER-muodon versio **1.1.2**.
2.  Valitse toimintoruudussa **Tuo**.
3.  Vahvista valitsemalla **Kyllä**, että muodon tämän version aiemmin luodut sovelluskohtaiset parametrit korvataan.
4.  Etsi versioon **1.1.1** viedyt sovelluskohtaiset parametrit sisältävä tiedosto valitsemalla **Selaa**.
5.  Valitse **OK**.

    ER-muodon versiossa **1.1.2** on nyt ne sovelluskohtaiset parametrit, jotka määritettiin alun perin versioon **1.1.1**.
    
    Huomaa, että ER-muodon sovelluskohtaiset parametrit ovat yrityskohtaisia. Yhdelle yritykselle määritettyjen sovelluskohtaisten parametrien käyttäminen uudelleen toisessa yrityksessä edellyttää, että ne viedään, kun olet kirjautuneena ensimmäiseen yritykseen ja tuodaan sitten, kun olet kirjautunut toiseen yritykseen.

    Voit siirtää tällä tavoin myös yhteen Financen esiintymään määritettyjä ER-muotoon liittyviä sovelluskohtaisia parametreja toiseen Financen esiintymään.

    Ota huomioon, että jos määrität yhden ER-muodon version sovelluskohtaiset parametrit ja tuot saman muodon korkeamman version nykyiseen Financen esiintymään, aiemmin luotuja sovelluskohtaisia parametreja ei käytetä tuodussa versiossa.
    
    Ota myös huomioon, että kun valitset tuotavan tiedoston, kyseisen tiedoston sovelluskohtaisten parametrien rakennetta verrataan vastaavan tuotavaksi valitun ER-muodon **Haku**-tyypin tietolähteen rakenteeseen. Tuonti tehdään, kun kunkin sovelluskohtaisen parametrin rakenne vastaa vastaavan tietolähteen rakennetta tuotavaksi valitussa ER-muodossa. Jos rakenteet eivät vastaa toisiaan, saat varoitussanoman, joka ilmaisee, että tuontia ei voi tehdä. Jos pakotat tuonnin, valitun ER-muodon aiemmin luodut sovelluskohtaiset parametrit tyhjennetään ja ne on määritettävä alusta alkaen.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Sovelluskohtaisten parametrien ja ER-muodon välinen suhde

ER-muodon ja sen sovelluskohtaisten parametrien välinen suhde muodostetaan ER-muodon yksilöivällä esiintymästä riippumattomalla tunnuskoodilla. Niinpä kun poistat ER-muodon Financesta, ER-muotoon määritetyt sovelluskohtaiset parametrit jäävät Financen nykyiseen esiintymään. Niitä voidaan käyttää, kun ER-perusmuoto tuodaan uudelleen Financen esiintymään.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Sovelluskohtaisten parametrien käyttäminen ER-kehystä käyttämällä

Edellisessä esimerkissä olet käyttänyt ER-muodon sovelluskohtaisia parametreja ER-kehyksen avulla. Tällä tavoin et kuitenkaan voi rajoittaa tietyn ER-muodon sovelluskohtaisten parametrien käyttöä. Jos kyseisiä rajoituksia on käytettävä, toimi seuraavasti: 

1.  Käytä joko aiemmin luotua **ERSolutionAppSpecificParametersDesigner**-valikkovaihtoehtoa uudelleen tai käytä omaa **ERSolutionAppSpecificParametersDesigner**-valikkovaihtoehtoa.

    ![Visual Studio -sivu.](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  Noudata seuraavia ohjeita:

    1.  Luo uusi valikkovaihtoehdon painike ja linkitä se vastaavaan **ERSolutionTable**-taulukon tietueeseen määrittämällä sen **Tietolähde**-ominaisuudeksi **ERSolutionTable**.
    
        ![Visual Studio -sivu.](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  Luo yksinkertainen painike ja korvaa **Napsautus**-menetelmä seuraavassa esimerkissä kuvatulla tavalla.
    
        Tällä tavoin voit määrittää yksilöivän ratkaisutunnuksen (määritetty **GUID**-arvon avulla) sallimaan vain tietyn ER-muodon ja siitä johdettavien kopioiden sovelluskohtaisten parametrien käyttämisen.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[ER-muotojen määrittäminen käyttämään yrityskohtaisesti määritettyjä parametreja](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
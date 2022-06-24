---
title: Vastaavaa tulosta ei löytynyt
description: Tässä artikkelissa kerrotaan, miten verolaskentapalvelun "Vastaavaa tulosta ei löytynyt" -virhettä korjataan.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845141"
---
# <a name="no-matching-result-could-be-found"></a>Vastaavaa tulosta ei löytynyt

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten tehdään vianetsintää, kun verolaskentapalvelun "Vastaavaa tulosta ei löytynyt" -virhettä korjataan.

## <a name="symptom"></a>Oire

Näkyviin tulee seuraava virhesanoma: Otsikko/Rivit - 1, Veroryhmä, vastaavia tuloksia ei löydy."

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Syy

Ongelma ilmenee, kun Regulatory Configuration Servicen (RCS) toimintoasetus on virheellinen.

## <a name="troubleshoot"></a>Vianmääritys

1. Lataa vianmääritystiedosto. Lisätietoja on kohdassa [Virheenkorjaustilan ottaminen käyttöön vianetsintään](tcs-troubleshooting-enable-debug-mode.md).
2. Korjaa asetusongelma vertaamalla veropalvelun laskennan syötettä toiminnon asetuksiin.

    Seuraavassa esimerkissä näkyy veropalvelun laskennan syöte.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Seuraavassa taulukossa on luettelo veroryhmän käytettävyydestä RCS:ssä.

    | Header.Business process | Lines.Business Unit | Header.Ship From Zip Code | Veroryhmä |
    |-------------------------|---------------------|---------------------------|-----------|
    | Kirjauskansio                 |                     |                           | Ryhmä A   |
    | Myynti                   |                     | 30160                     | Ryhmä B   |

    Veropalvelulaskelman syötteen mukaan **liiketoimintaprosessin** arvo otsikossa on **Myynti** ja otsikkotietojen **Ship From Zip Code** -arvo on **30159**. Tämä syöte perustuu RCS:n käytettävyyssääntöjen määritykseen. Koska vastaavaa riviä ei ole, virhe ilmenee.

    > [!NOTE]
    > Jos käytettävyyssäännön arvo on tyhjä, sääntö koskee mitä tahansa arvoa.

## <a name="mitigation"></a>Lievennys

Vältä virhe seuraavien ohjeiden avulla.

1. Siirry RCS:ssä kohtaan **Globalisointiominaisuudet** \> **Veronlaskenta**.
2. Luo uusi versio ominaisuudesta.
3. Lisää vastaavien tietojen rivi.

    | Header.Business process | Lines.Business Unit | Header.Ship From Zip Code| Veroryhmä |
    |-------------------------|---------------------|--------------------------|-----------|
    | Kirjauskansio                 |                     |                          | Ryhmä A   |
    | Myynti                   |                     | 30160                    | Ryhmä B   |
    | Myynti                   |                     | 30159                    | Ryhmä B   |

4. Julkaise ominaisuuden määritysversio.
5. Valitse Microsoft Dynamics 365 Financessa **Vero** \> **Asetukset** \> **Veromääritys** \> **Verolaskennan parametrit** ja valitse uusi versio.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

# Mondial Relay API client

The gem works as an interface to the
[Mondial Relay Web service](https://api.mondialrelay.com/Web_Services.asmx).
As for this version only the *drop-off* point
[search](https://api.mondialrelay.com/Web_Services.asmx?op=WSI3_PointRelais_Recherche)
is available.

### Progress:
- ✅ `WSI3_PointRelais_Recherche`
- ❌ `WSI2_CreationExpedition`
- ✅ `WSI2_CreationEtiquette`
- ❌ `WSI2_RechercheCP`
- ❌ `WSI2_TracingColisDetaille`
- ❌ `WSI3_GetEtiquettes`
- ❌ `WSI2_STAT_Label`

### Documentation
Documentation can be generated by using `yard`.

### Contribution
- Each endpoint (operation) should be documented.
- Each entity (e.g. *drop-off* point) should provide a public interface to query the API.
For example, a gem user could work with *drop-off* points like this:
    ```ruby
    MondialRelay::DropOffPoints.search(
      Pays: 'FR',
      CP: '75010',
      Latitude: '48.8711706',
      Longitude: '02.3602504'
    )
    ```

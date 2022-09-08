# Esperimento di applicazione web su SAP Cloud Foundry.

Crea un endpoint POST che riceve un PDF come payload, e restituisce un oggetto JSON con la lista dei valori dei barcode rilevati nella prima pagina del documento.

---

## Istruzioni:

- Creare [account trial](https://account.hanatrial.ondemand.com/trial/#/home/trial).
- Installare [tools cli](https://github.com/cloudfoundry/cli/releases) per Cloud Foundry.
- `cf api https://api.cf.eu20.hana.ondemand.com` (usare endpoint cf corretto per il proprio trial)
- `cf login`
- `cf push`

---

## Note:
Questa installazione utilizza `conda-forge`, poichè è l'unico modo che ho trovato per installare i binari di `poppler` (su `pip` non ci sono). La fase di installazione è MOLTO pesante, quindi bisogna predisporre per l'istanza almeno 3 o 4 GB di RAM. Una volta installata la si può ridurre dall'interfaccia web di Cloud Foundry (a regime l'applicazione non dovrebbe richiedere più di 200 MB di RAM, più o meno). L'installazione a regime occupa circa 1GB di disco (sempre causa `conda-forge`).

---

## Risorse varie:

https://developers.sap.com/tutorials/btp-cf-buildpacks-python-create.html

https://adamtheautomator.com/flask-web-server/

https://www.ianhuston.net/2014/11/python-on-cloud-foundry/

https://docs.cloudfoundry.org/devguide/deploy-apps/manifest-attributes.html

https://techtutorialsx.com/2020/01/01/python-pyzbar-detecting-and-decoding-barcode/
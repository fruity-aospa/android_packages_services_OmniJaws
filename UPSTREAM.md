# Asteroids weather provider integration

The coherent Java/AndroidX frontend is based on crDroid OmniJaws 16.0-qpr1 at
fe3e95d465e7367402e60f7a582592ef5a79d23f:
https://github.com/crdroidandroid/android_packages_services_OmniJaws/tree/fe3e95d465e7367402e60f7a582592ef5a79d23f

Weather backend/provider/model sources and Google condition vectors come from
crDroid 17.0 at c304570bc98834a6bc93eed39062da9087db30fd:
https://github.com/crdroidandroid/android_packages_services_OmniJaws/tree/c304570bc98834a6bc93eed39062da9087db30fd

Existing authorship/license headers are retained. The app-local client is adapted
from the existing Launcher3 standalone OmniJaws client, carrying its OmniROM and
crDroid authorship. It removes the dependency on a crDroid framework class.
No Axion toolkit or shared crDroid resources are required.

The app starts disabled. Location permissions are requested by setup rather than
pregranted. Background location is explained and opened through app permissions
after a foreground grant; a custom city requires no device location permission. Weather/provider updates retain the current 17.0 backend's location,
custom-city, provider-change and offline unit-conversion handling. The legacy
frontend exposes MET Norway, OpenWeatherMap and keyless Open-Meteo with existing
provider IDs preserved. Current Pixel weather vectors use the supported
`google_new` prefix and its manifest metadata.

Asteroids product selection and manifest ownership are outside this repository.

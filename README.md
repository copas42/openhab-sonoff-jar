The method I used to build these:



git clone https://github.com/openhab/openhab-addons.git

cd openhab-addons

git checkout 4.3.x

echo bundles/org.openhab.binding.sonoff/** >>.gitignore

cd bundles

git clone https://github.com/copas42/openhab-4.x-sonoff.git org.openhab.binding.sonoff

cd org.openhab.binding.sonoff

edit pom.xml and set version from parent pom

mvn spotless:apply

mvn clean package

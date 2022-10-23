# AndroidWithFastLane
Fastlane Dependencies install on windows
fastlane supports Ruby versions 2.5 or newer. Verify which Ruby version you're using on command prompt:
ruby --version
If ruby version not found, then install Ruby+Devkit 3.1.X (x64) installer from https://rubyinstaller.org/downloads/ . After installing the .exe file , click finish and it will open command prompt and select 3rd option of “MSYS2 and MINGW development toolchain” and press enter. After the installation close the command prompt
Then download ruby gems zip file from https://rubygems.org/pages/download and install it by running setup . 
Open command prompt again.
And check ruby –version and gem -v on command prompt to check successful installation. Then install bundler by running below command on command prompt
gem install bundler
gem install Fastlane
After that Navigate your terminal to your project's directory and run
bundle init
echo 'gem "fastlane"' >> Gemfile
bundle install
Then run the below commands
Fastlane init
You'll be asked to confirm that you're ready to begin, and then for a few pieces of information. To get started quickly:
1.	Provide the package name for your application when asked (e.g. com.rumman)
2.	Press enter when asked for the path to your json secret file
3.	Answer 'n' when asked if you plan on uploading info to Google Play via fastlane 
That's it! fastlane will automatically generate a configuration for you based on the information provided.
You can see the newly created ./fastlane directory, with the following files:
•	Appfile which defines configuration information that is global to your app
•	Fastfile which defines the "lanes" that drive the behavior of fastlane

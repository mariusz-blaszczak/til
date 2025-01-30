ja kiedyś próbowałem z tym .gem ale mi się nie udało
 
No a mi się właśnie udało
 
po pierwsze, w gemspec trzeba zrobić tak, żeby sam gemspec też był spakowany
 
  spec.files         = %w[README.md] + Dir.glob("bin/**/*") + Dir.glob("lib/**/*") + Dir.glob("iss-tririga-connector.gemspec")
 
po drugie, gema kopiuję do ./custom_gems/gems
 
po trzecie robię gem generate_index --directory $APP_ROOT/custom_gems
 
a potem w Gemfile projektu ubs mam jeszcze to: 
 
gem 'iss-tririga-connector', source: "file:///app/custom_gems/"
 
to mi pozwoli ładniej zarządzać gemami i dołączać kilka, gdybym miał potrzebę
 

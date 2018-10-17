### rack-secure-upload
---

https://github.com/dtaniwaki/rack-secure-upload

```
gem "rack-secure-upload"

wget -c http://files.avast.com/files/linux/avast4workstation-1.3.0-1.i586.rpm
sudo yum localinstall avast4workstation-1.3.0.1-i586.rpm
avast -V
avast-update

wget http://download.f-secure.com/webclub/f-secure-linux-security-10.00.60.tar.gz
tar xvzf f-secure-linux-security-10.00.60.tar.gz
sudo ./f-secure-linux-security-10.00.60/f-secure-linux-security-10.00.60

```

```ruby
require 'rack-secure-upload'
use Rack::secureUpload::Middleware, :fsecure
run MyApp

# config/application.rb
moudle MyApp
  class Application < Rails::Applicaiton
    config.middleware.insert_before ActionDispatch::ParamsParser, Rack::SecureUpload::Middleware, :avast
  end
end

use Rack::SecureUpload::Middleware, :fsecure, {foo: :bar}

```

```

```

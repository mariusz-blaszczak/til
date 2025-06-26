
```ruby
require 'sinatra'
require 'json'

set :port, 4567
set :bind, '0.0.0.0' # ← This line allows access from outside the host. host.docker.internal
set :host_authorization, { permitted_hosts: [] }

post '/anything' do
  content_type :json
  headers 'Retry-After' => '120', 'X-Custom-Header' => 'Test-Value'

  status 503
  { error: 'Service Unavailable' }.to_json
end
```

```text
ruby sinatra.rb
```

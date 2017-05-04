# How to download images from website using bash script

## 1. Prepare urls
### Go to website
https://thebibleproject.com/resources/?swoof=1&product_tag=posters&paged=1

### In web dev tools
```javascript
$('.item-buttons').find('a:contains("Download")').map(function(e,v ){ return ($(v).attr('href')) }).toArray()
```

## 2. Copy result to sublime
### Replace with reg exp option
`"\n[\d]*\n:`
with: 
`" `

## 3. Create bash script file
and copy array from sublime to links array.
```bash
links=( "url" "url" ... )
for i in "${links[@]}"
do
	wget -nc $i
done
```

## 4. Change chmod of file to executable with
`chmod u+x filename`

## 5. Execute file
`./filename`


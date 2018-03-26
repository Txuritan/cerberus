src = "src/"

dist = "docs/"
file = "index"

task :watch do |t, args|
	system "sass --watch #{src}:#{dist}"
end

task :compile do |t, args|
	puts "Building cerberus.css..."
	system "sass #{src}#{file}.scss:#{dist}cerberus.css"

	puts "Building cerberus.min.css..."
	system "sass #{src}#{file}.scss:#{dist}cerberus.min.css --style compressed"

	puts "Building index.html..."
	system "haml #{src}index.haml #{dist}index.html"
end

task :serve do |t, args|
	system "ruby -run -e httpd . -p 5000"
end

setup:
	@echo '🔥 Making CodeIgniter 4 setup... 🔥'
	@composer create-project codeigniter4/appstarter src
	@chmod -R 0777 ./src/writable

clean:
	@echo -e '❗🛑 --make clean-- 🛑❗\n' 
	@echo -e '❗🛑 Will remove the folder from the project and the database 🛑❗\n'
	@echo -e '❗🛑 Are you sure about that? 🛑❗\n'
	@sudo rm -rf ./data
	@sudo rm -rf ./src

d-start:
	@echo '🐋🚀 Starting containers... 🚀🐋'
	@docker-compose --env-file ./.docker.env up -d

d-stop:
	@echo '🐋🛑 Stopping containers... 🛑🐋'
	@docker-compose --env-file ./.docker.env down

d-rebuild:
	@echo '🐋🏗️ Rebuilding and starting containers... 🏗️🐋'
	@docker-compose --env-file ./.docker.env up -d --build
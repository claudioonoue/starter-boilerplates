setup:
	@echo '🔥 Making CodeIgniter 4 setup... 🔥'
	@composer create-project codeigniter4/appstarter src
	@chmod -R 0777 ./src/writable

clean:
	@echo '❗❗❗ --make clean-- Will remove the folder from the project and the database ❗❗❗'
	@echo '❗❗❗                        Are you sure about that?                         ❗❗❗'
	@sudo rm -rf ./data
	@sudo rm -rf ./src

d-build:
	@echo '🐋🏗️ Building containers... 🏗️🐋'
	@docker-compose --env-file ./.docker.env build

d-start:
	@echo '🐋🚀 Starting containers... 🚀🐋'
	@docker-compose --env-file ./.docker.env up -d

d-stop:
	@echo '🐋🛑 Stopping containers... 🛑🐋'
	@docker-compose --env-file ./.docker.env down
	
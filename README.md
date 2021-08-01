# springprojectaslibarary


bootJar {
	enabled = false
//	archiveFileName = "${archiveBaseName.get()}.${archiveExtension.get()}"
}
//
jar {
	enabled = true
	archiveFileName = "${archiveBaseName.get()}.${archiveExtension.get()}"

}




spring.main.allow-bean-definition-overriding: true

@EntityScan(
    basePackages = {"main.application.repositories.entities", "fully.package.name.of.library.repositories.entities"})
@ComponentScan({"main.application.components.*", "fully.package.name.of.library.components*"})
@EnableJpaRepositories(
    basePackages = {"main.application.repositories", "fully.package.name.of.library.repositories"})

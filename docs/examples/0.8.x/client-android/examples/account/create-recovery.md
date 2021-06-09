import io.appwrite.Client
import io.appwrite.services.Account

val client = Client(context)
  .setEndpoint("https://[HOSTNAME_OR_IP]/v1") // Your API Endpoint
  .setProject("5df5acd0d48c2") // Your project ID

val accountService = Account(client)
val response = accountService.createRecovery("email@example.com", "https://example.com")
val json = response.body?.string()
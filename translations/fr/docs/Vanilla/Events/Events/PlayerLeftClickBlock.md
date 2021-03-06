# Clic-gauche du joueur

L'événement PlayerLeftClickBlock est lancé chaque fois qu'un joueur clique sur un bloc.  
Il peut être annulé pour empêcher tout autre événement de se produire. Si le joueur maintient le clic gauche, l'événement se déclenchera à nouveau même s'il a été annulé. L'annulation de cet événement empêchera le clic gauche d'être enregistré, empêchant le cassage de bloc (mais pas en mode créatif). Si l'événement est annulé, un résultat spécifique de succès, d'échec ou de passe peut être fourni. Par défaut, le résultat est passé.

## Event Class
Vous devrez lancer l'événement dans l'en-tête de la fonction comme cette classe:  
`crafttweaker.event. layerLeftClickBlockEvent`  
Vous pouvez, bien sûr, également [importer](/AdvancedFunctions/Import/) la classe avant et utiliser ce nom alors.

## Event interface extensions
Les événements PlayerLeftClickBlock implémentent les interfaces suivantes et peuvent également appeler toutes leurs méthodes/getters/setters :

- [IEventCancelable](/Vanilla/Events/Events/IEventCancelable/)
- [PlayerInteract](/Vanilla/Events/Events/PlayerInteract/)
- [IPlayerEvent](/Vanilla/Events/Events/IPlayerEvent/)


## ZenGetters & ZenSetters
The following information can be retrieved from the event:

| ZenGetter                  | ZenSetter                  | type                                   |
| -------------------------- | -------------------------- | -------------------------------------- |
| `hitvector`                |                            | [IVector3d](/Vanilla/World/IVector3d/) |
| `Bloc d'utilisation`       | `Bloc d'utilisation`       | chaîne ("allow" / "deny" / "default")  |
| `useitem`                  | `useitem`                  | chaîne ("allow" / "deny" / "default")  |
| `Résultat de l'annulation` | `Résultat de l'annulation` | chaîne ("success" / "pass" / "fail")   |

## ZenMethods

- `event.cancel()` sets the event as cancelled.

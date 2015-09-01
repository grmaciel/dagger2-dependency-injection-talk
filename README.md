# dependency-injection-talk

## Tightly coupled code (bad)!
- Global state
- Statics everywhere
- Work in constructors
- Using new

## IoC - Inversion of Control

## Dependency Injection
- Expose your dependencies in your constructors
and pass them in.
- Client flexibility and modularization
- Decreases coupling
- Different modules for app/test context
- Depend upon abstractions!

**Bad** (tightly coupled)
```
public class BadAssEnemy {
   private IWeapon weapon;
   private IArmor armor;
   
   public BadAssEnemy() {
       this.weapon = new Axe();
       this.armor = new LeatherArmor();
   }
}
```

**Good** (loosely coupled)
```
public class BadAssEnemy {
   private IWeapon weapon;
   private IArmor armor;
   
   public BadAssEnemy(IWeapon weapon, IArmor armor) {
       this.weapon = weapon;
       this.armor = amor;
   }
}
```

## Show me the code!

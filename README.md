# dependency-injection-talk

## Tightly coupled code (bad)!
- Global state
- Statics everywhere
- Work in constructors
- Using new

## IoC - Inversion of Control
"Inversion of Control is a key part of what makes a framework different to a library. A library is essentially a set of functions that you can call, these days usually organized into classes. Each call does some work and returns control to the client.

A framework embodies some abstract design, with more behavior built in. In order to use it you need to insert your behavior into various places in the framework either by subclassing or by plugging in your own classes. The framework's code then calls your code at these points."

- Martin Fowler

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

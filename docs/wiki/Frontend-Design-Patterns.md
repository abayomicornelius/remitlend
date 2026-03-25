# Frontend Standard Library & Design Patterns

RemitLend uses a modular, atomic design pattern for its frontend to ensure consistency across borrower and lender interfaces.

## Core Design Principles
- **Design System Consistent**: All UI elements derive from the core design language established in `@stellar/design-system` (Stellar Design System - SDS).
- **Type Safe**: 100% TypeScript coverage for props and state.
- **Client Components**: Interactive UI logic is strictly separated into `"use client"` files.

## Atomic Components

### 1. Button (`/components/ui/Button.tsx`)
A flexible primitive that handles loading states, icons, and common variants.

**Usage:**
```tsx
import { Button } from "@/app/components/ui/Button";

<Button 
  variant="primary" 
  onClick={handleMint} 
  isLoading={isMinting}
  leftIcon={<PlusIcon />}
>
  Mint NFT
</Button>
```

### 2. Card (`/components/ui/Card.tsx`)
The standard container for dashboards and lists.

**Prop Structure:**
- `CardHeader` / `CardTitle` / `CardDescription`
- `CardContent`
- `CardFooter`

### 3. Modal (`/components/ui/Modal.tsx`)
For focused user actions (Confirmation, Loan Request Forms).

---

## State Management & Hooks

### Wallet Integration
Standard pattern for connecting to Stellar Wallets:

```tsx
import { useWallet } from "@/hooks/useWallet";

const { address, connect, disconnect } = useWallet();
```

### Transaction Simulation
Before many on-chain actions, we use the `TransactionSimulationModal` template to show users exactly what will happen (estimated fees, state changes).

## Folder Structure Conventions
- `@/app/components/ui`: Pure, atomic components (The "Standard Library").
- `@/app/components/borrower`: Feature-specific logic.
- `@/app/components/global_ui`: Layout items (Navbar, Footer, Notifications).

## Styling Guide (Tailwind)
- **Colors**: Use custom tokens (e.g., `text-zinc-50`, `bg-blue-600`).
- **Layout**: Follow the `Layout.Inset` pattern for standardized margins.
- **Responsiveness**: Mobile-first approach with `max-[480px]` or `sm:` breakpoints.

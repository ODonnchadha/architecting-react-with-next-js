# Architecting React Applications with Next.js

- LAYING THE FOUNDATION:
    - Version check:
        - React 18.3.1. Next.js 14.2.5 Node.js 18.7.1.
        - JavaScript, HTML & CSS, React.
    - Introduction:
        - Next.js and other frameworks. Advanced features. 
        - Suspense. Server-side rendering & server components.
        - Refactoring and best practices.
    - React decisions:
        - Rich user interfaces.
        - Routing. Data fetching. SSR. SEO. Testing.
            - Performance. Deployments.
        - Organization of app structure & components.
            - Data flow and state management.
        - Scalable. Maintainable. Modular and reuseable. Collabrative.
    - Architectural design:
        - Simple to understand and maintain. Use the correct tools.
        - State-managed effectively. Keep state local.
            - State management libraries & custom hooks.
        - Security.
        - Performance. Server-side rendering.
        - Scalability of code.
    - DEMO: Bethany's Pie Shoppe.

- LEVERAGING NEXT.JS & OTHER FRAMEWORKS:
    - Building blocks:
        - UI. Routing. Data fetching. Rendering. (Client versus server.)
        - Performance and scalability. Integration and infrastructure.
        - Build React app using a framework. Open source. COmmunity support.
    - Next.js & Remix:
        - Bundling, compiling, optimization. File-system-based routing.
            - React server components.
            ```javascript
                import Albums from './albums'
                async function getArtist(username: string) {
                    const res = await fetch(`https://api.example.com/artist/${username}`)
                    return res.json()
                }
                // Server component.
                export default async function Page({
                    params: { username },
                } : {
                    // Fetch artist from cpmponent
                    const artist = getArtist(username)

                    return (
                        <>
                            <h1>{artist.name}</h1>
                            <Suspense fallback={<div>Loading...</div>}>
                                <Albums artist={artist.id}/>
                            </Suspense>
                        </>
                    )
                })
            ```
            - RSC run entirely on the server. Speed. Overall performance.
            - Can fetch data directly from the component, make server calls.
            - DB queries. And write to the DB from the server-side component.
        - Remix: UI-focused. Built on top of React router.
            - Nested routes, allowing the app to fetch data quicker.
            - Server build. (One bundle.) CLient build. (Multiple bundles.)
        - Shared:
            - Full-stack React applications. File-based routing.
                - Enhanced data loading. Focused on performance.
    - Next.js Features:
        - File-system routing.
        - Client and server-side rendering. Page-by-page basis.
        - Data fetching.
        - Image and font optimization.
        - React server components.
        - Middleware. FF. Authentication.